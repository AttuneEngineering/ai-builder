# LLAVA Vision by Attune Engineering
---

## ONE-CLICK TEMPLATE
Deploy the model to Runpod to host your own inference-ready endpoint with multimodal capabilities.

#### *[Template Link](https://runpod.io/gsc?template=aajbtuv52q&ref=zdeyr0zx)*

*Use Attune Engineering's [Runpod Affiliate Link](https://runpod.io?ref=zdeyr0zx) affiliate link to sign up for Runpod and help support our team to keep building and sharing systems with AI with free GPU credits!*

_note_ You will need to perform an additional step of launching the Flask server to start the API endpoint once your Runpod deployment is running. This is detailed in the *[Inference](#inference)* section below.

---

## ABOUT
Configured by [Reed Bender](https://reedbender.com) with [Attune Engineering](https://attuneengineering.com) as an open alternative to GPT-4-vision. This template is intended to simplify the process of deploying open-source vision models such as LLaVA to Runpod GPUs and making them available via an API.

This One-Click-Template is built off the [Docker Image for LLaVA](https://github.com/ashleykleynhans/llava-docker) (Large Language and Vision Assistant). LLAVA is a multimodal LLM trained on both image and text input, making it an excelent model for understanding context from images. 

### Available Models

> [!IMPORTANT]
> If you select a 13B or larger model, CUDA will result in OOM errors with a GPU that has less than 48GB of VRAM. At least a single A6000 or larger is recommended for 13B models. When running the 34B model, 96GB of VRAM or larger is recommended.

You can add an environment called MODEL to your Docker container to specify the model that should be downloaded. If the `MODEL` environment variable is not set, the model will default to the 7B parameter `Mistral-7B` implementation of `LLaVA-1.6`.

#### LLaVA-v1.6

| Model                                                                            | Environment Variable Value       | Version    | LLM           | Default |
|----------------------------------------------------------------------------------|----------------------------------|------------|---------------|---------|
| [llava-v1.6-vicuna-7b](https://huggingface.co/liuhaotian/llava-v1.6-vicuna-7b)   | liuhaotian/llava-v1.6-vicuna-7b  | LLaVA-1.6  | Vicuna-7B     | no      |
| [llava-v1.6-vicuna-13b](https://huggingface.co/liuhaotian/llava-v1.6-vicuna-13b) | liuhaotian/llava-v1.6-vicuna-13b | LLaVA-1.6  | Vicuna-13B    | no      |
| [llava-v1.6-mistral-7b](https://huggingface.co/liuhaotian/llava-v1.6-mistral-7b) | liuhaotian/llava-v1.6-mistral-7b | LLaVA-1.6  | Mistral-7B    | yes     |
| [llava-v1.6-34b](https://huggingface.co/liuhaotian/llava-v1.6-34b)               | liuhaotian/llava-v1.6-34b        | LLaVA-1.6  | Hermes-Yi-34B | no      |

#### LLaVA-v1.5

| Model                                                                            | Environment Variable Value       | Version   | Size | Default |
|----------------------------------------------------------------------------------|----------------------------------|-----------|------|---------|
| [llava-v1.5-7b](https://huggingface.co/liuhaotian/llava-v1.5-7b)                 | liuhaotian/llava-v1.5-7b         | LLaVA-1.5 | 7B   | no      |
| [llava-v1.5-13b](https://huggingface.co/liuhaotian/llava-v1.5-13b)               | liuhaotian/llava-v1.5-13b        | LLaVA-1.5 | 13B  | no      |
| [BakLLaVA-1](https://huggingface.co/SkunkworksAI/BakLLaVA-1)                     | SkunkworksAI/BakLLaVA-1          | LLaVA-1.5 | 7B   | no      |

*note*: Although the container logs may say that the Container is READY, the model worker will still need to download the model the first time you create the pod. This can take quite a bit of time, depending on the GPUs provisioned.

---

## LOGS
LLaVA creates log files, and you can tail the log files instead of killing the services to view the logs.

| Application  | Log file                          |
| :----------- | :-------------------------------- |
| Controller   | /workspace/logs/controller.log    |
| Webserver    | /workspace/logs/webserver.log     |
| Model Worker | /workspace/logs/model-worker.log  |

For example:
    ```
    tail -f /workspace/logs/webserver.log
    ```

---

## INFERENCE
### 1. Starting Flask
The Flask server must be started inside of your Runpod instance once all of the model weights have been downloaded and the model is ready at port 3000. Starting the Flask server will enable API requests to be sent through port 5000. 

In the Runpod web portal, click the option for a *Web Terminal*. This will load a virtual connection to your provisioned GPU via your web browser. Run through the following bash commands:

    ```bash
    ### STOP EXISTING WORKERS AND CONTROLLER TO FREE VRAM
    fuser -k 10000/tcp 40000/tcp

    ### INSTALL DEPENDENCIES
    source /workspace/venv/bin/activate
    pip3 install flask protobuf
    cd /workspace/LLaVA
    export HF_HOME="/workspace"
    python -m llava.serve.api -H 0.0.0.0 -p 5000

    ### TAKE NOTE OF RUNPOD ID
    ```
The Runpod ID will be used to connect to the now-deployed inference endpoint!

### 2. Sending Requests
To now query against this endpoint, we can configure the following python script:

    ```python
    import json
    import requests
    import base64

    RUNPOD_ENDPOINT = f"https://{RUNPOD_ID}-5000.proxy.runpod.net/inference"
    IMAGE_PATH = "/my/image/path.png"
    QUESTION = "Describe this image."

    def encode_image_to_base64(self,
                                image_path):
        with open(image_path, 'rb') as image_file:
            return str(base64.b64encode(image_file.read()).decode('utf-8'))

    ### FORMAT INPUT
    payload = {
        'model_path': 'liuhaotian/llava-v1.5-7b', ### TO DIVERGE FROM DEFAULT
        'image_base64': encode_image_to_base64(IMAGE_PATH),
        'prompt': QUESTION,
        'temperature': 0.2,
        'max_new_tokens': 300
    }

    ### SEND TO MODEL
    response = requests.post(
        RUNPOD_ENDPOINT,
        json=payload,
    )
    text_response = r.json()["response"]
    print(text_response)
    ```

You can edit the *System Prompt* by adjusting the question that goes along with the image path to extract or focus on certain elements within the image. 

---