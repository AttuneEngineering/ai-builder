<div align="center">
  <img src="assets/images/ai-builder-header.jpg" alt="AI-Builder" />
</div>

<div align="center">
    <h1>AI Builder</h1>
</div>

<div align="center">
  <!-- Build Status -->
  <a href="https://github.com/AttuneEngineering/ai-builder/actions">
    <img src="https://github.com/AttuneEngineering/ai-builder/actions/workflows/main.yml/badge.svg" alt="Build Status" />
  </a>
  <!-- Code Size -->
  <a href="">
    <img src="https://img.shields.io/github/languages/code-size/attuneengineering/ai-builder" alt="Code Size" />
  </a>
  <!-- Contributers -->
  <a href="https://github.com/attuneengineering/ai-builder/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/attuneengineering/ai-builder.svg" alt="Contributers" />
  </a>
  <!-- GitHub Issues -->
  <a href="https://github.com/attuneengineering/ai-builder/issues">
    <img src="https://img.shields.io/github/issues/attuneengineering/ai-builder.svg" alt="GitHub Issues" />
  </a>
  <!-- Forks -->
  <a href="https://github.com/attuneengineering/ai-builder/network/members">
    <img src="https://img.shields.io/github/forks/attuneengineering/ai-builder.svg" alt="Forks" />
  </a>
  <!-- Followers -->
  <a href="https://github.com/attuneengineering?tab=followers" target="_blank">
    <img src="https://img.shields.io/github/followers/attuneengineering?style=social" alt="Follow on GitHub">
  </a>
  <!-- Stars -->
  <a href="https://github.com/attuneengineering/ai-builder/stargazers" target="_blank">
    <img src="https://img.shields.io/github/stars/attuneengineering/ai-builder?style=social" alt="GitHub stars">
  </a>
  <!-- Commit Activity -->
  <a href="https://github.com/attuneengineering/ai-builder/commits" target="_blank">
    <img src="https://img.shields.io/github/commit-activity/m/attuneengineering/ai-builder" alt="GitHub commits">
  </a>
  <!-- Last Commit -->
  <a href="https://github.com/attuneengineering/ai-builder/commits" target="_blank">
    <img src="https://img.shields.io/github/last-commit/attuneengineering/ai-builder" alt="GitHub last commit">
  </a>
  <!-- License -->
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License" />
  </a>
</div>

<div align="center">
    <p>For support, either <a href="https://github.com/AttuneEngineering/ai-builder/issues/new/choose"> add an issue</a> or reach out to <a href="mailto:contact@attuneengineering.com">contact@attuneengineering.com</a>.</p>
    <a href="https://www.youtube.com/channel/UCNMrLvZji3XeWghxsAWKXjg"><img src="https://img.shields.io/youtube/channel/subscribers/UCNMrLvZji3XeWghxsAWKXjg?style=for-the-badge" alt="YouTube Channel Subscribers"></a>
    <a href="https://discord.gg/sAbbvBNU"><img src="https://img.shields.io/discord/1199192124290257058.svg?style=for-the-badge&label=Join%20Community&color=7289DA" alt="Join Community Badge"/></a><br>
    <em>created and maintained by <a href="https://github.com/mrbende" target="_blank">Reed Bender</a></em></p>
    <a href="https://gitpod.io/#https://github.com/AttuneEngineering/ai-builder" target="_blank"><img src="https://gitpod.io/button/open-in-gitpod.svg" alt="Open-in-Gitpod"></a>
</div>
</div>

---

### Abstract

The `AI Builder` repository is a template from which you can engineer your own application with open source generative AI. This codebase forms the cornerstone of Attune Engineering's [collection of private repositories](https://attuneengineering.com/source-code.html) for designing software architectures with Large Language Models. 

Within this repository you'll find:
  * **Server deployments** for renting <a href="https://runpod.io?ref=zdeyr0zx" target="_blank">Runpod</a> GPU servers and serving open-source LLMs;
  * **Inference scripts** for communicating with your API endpoints and integrating your models into your software;
  * **DevOps configurations** for managing development environments and workflow automations with Docker and Gitpod;
  * **Multimodal templates** for running LLMs for image comprehension as an open alternative to GPT-4-Vision;
  * **Streamlit frontends** for testing your creations locally in your browser.

This toolkit-based approach to interfacing with LLMs makes it easier to build complex architectures around your own fine-tuned open source LLMs. While OpenAI's API will continue to be the cheapest option for most all use cases - _because_ they can serve hundreds of thousands of people and amortise costs over concurrent requests - there are a few reasons why you may want to consider deploying your own API... if you
  * Cannot send data to OpenAI for privacy reasons;  _or_
  * Have a custom fine-tuned model you'd like to work with; _or_
  * Intend to build an application that can scale without being limited by OpenAI's API; _or_
  * Want to build a multi-model architecture across your own GPU hardware...

..._**this**_ is where you may want to rent a GPU server, set up your own API, and make queries to that API. If you're interested in this approach, we've created a collection of templates for you to hit the ground running!

---

# Table of Contents
- [API Server Deployments](#api-server-deployments)
- [Building Your Environment](#building-your-environment)
- [Usage](#usage)
- [License](#license)

---
---

# API Server Deployments

The largest barrier-to-entry for working with open source LLMs lies in provisioning your model to GPUs that can be made available at an API. <a href="https://runpod.io?ref=zdeyr0zx" target="_blank">Runpod</a> simplifies much of this process, and we have created a collection of ready-to-deploy templates to get you set up with an API endpoint in minutes.
  <ul>
    <li>See the complete list of server templates <a href="https://attuneengineering.com/models" target="_blank">here</a>.</li>
    <li>Includes Mixtral 8x7B, Llama 2, LLaVA Vision, and a plethora of others...</li>
    <li>Also includes models fine-tuned by Attune Engineering for multimodal document processing, function calling, and more!</li>
    <li>Find all of the README files in <code>server-docs/</code>.</li>
  </ul>

---
---

# Building Your Environment

### (a) Developing with Gitpod

Attune Engineering configures all of our repositories to work with [Gitpod](https://www.gitpod.io/docs/configure/workspaces), enabling you to deploy a preconfigured development environment to provisioned cloud resources. You are granted a free 50 hours of development per month, which is more than enough to get started.

<div align="center">
    <a href="https://gitpod.io/#https://github.com/AttuneEngineering/ai-builder" target="_blank"><img src="https://gitpod.io/button/open-in-gitpod.svg" alt="Open-in-Gitpod"></a>
</div>

Once working in Gitpod, you can launch the Jupyter Lab environment with the following...
  ```bash
  launch-jupyter
  ```

---

### (b) Running Docker on your local machine

1. Install [Docker](https://docs.docker.com/get-docker/) on your machine if it is not already installed.

2. Clone the `AI Builder` repository to your local machine.
    ```bash
    git clone git@github.com:AttuneEngineering/ai-builder.git
    cd ai-builder
    ```

3. Build the Docker image yourself _OR_ pull the image from Attune Engineering.
    ```bash
    ### BUILD FROM SOURCE...
    export REGISTRY_IMAGE="YOUR_GITHUB_USERNAME/ai-builder"
    docker build -f Dockerfile -t $REGISTRY_IMAGE:main .

    ### ...OR PULL FROM ATTUNE ENGINEERING
    export REGISTRY_IMAGE="ghcr.io/attuneengineering/ai-builder"
    docker pull $REGISTRY_IMAGE:main
    ```

4. Run the Docker container.
    ```bash
    docker run -it --rm -p 8888:8888 -p 8080:8080 $REGISTRY_IMAGE:main
    ```
    By default, this container will open an interactive bash environment. If you'd rather work in Jupyter, the following flag can be appended...
      * `--launch-jupyter`; launch a Jupyter Lab server on port 8888.

5. _optional_ Push the Docker image to your own Github Container Registry.
    This will require you to have a personal access token with `read:packages` and `write:packages` permissions. You can create a token [here](https://github.com/settings/tokens). Note that you'll also need to either fork the `AI Builder` repository or create a new repository in your own account.
    ```bash
    export GITHUB_TOKEN="xxx" 
    export REGISTRY_IMAGE="ghcr.io/YOUR_GITHUB_USERNAME/ai-builder"
    docker build -f Dockerfile -t $REGISTRY_IMAGE:main .
    echo $GITHUB_TOKEN | docker login ghcr.io -u YOUR_GITHUB_USERNAME --password-stdin
    docker push $REGISTRY_IMAGE:main
    ```
    _note_... Your `GITHUB_TOKEN` is already managed by the Github actions we are triggering with `.github/workflows/main.yml`, so it does not need to be added in addition.

    Additionally, this process can be automated with Github Actions. In order for the Github Workflows to successfully build the image and push it to your Github Container Registry, you must add the following to your `Repository Settings` --> `Secrets and Variables` --> `Actions` --> `Repository Secrets`...
    ```
    REGISTRY_IMAGE="ghcr.io/YOUR_GITHUB_USERNAME/ai-builder"
    ```

---

### (c) Building the environment locally

This is not ideal, as all of the source code is organized relative to the container's home directory within (`/workspace/ai-builder/src`). If you're simply looking to adapt the code to your own purposes, however, you can simply install the necessary requirements and update your environment's `PYTHONPATH` to point to your local `src` directory.
  ```bash
  pip install -r requirements.txt
  ```
    
---
---

# Usage 

### Setting API Keys 

> [!IMPORTANT]
> You must make the following API keys available as environment variables. This can be done by creating a `.env` file with the following keys, or otherwise by adding them to your environment.
  ```bash
  OPENAI_API_KEY="xxx"
  ```

This is all that is required to then instantiate the `AIBuilder` class, as defined in `src/builder.py`

### Building in Jupyter Lab

  ```bash
  ### IN GITPOD
  launch-jupyter

  ### LOCALLY BUILT IMAGE
  source /workspace/ai-builder/bin/jupyter-lab.sh
  ```
Check out `dev.ipynb` to get started.

### Testing with Streamlit

If you're looking to toy around with a web interface deployed to your local host via the Docker environment, you can launch the Streamlit app with the following...
  ```bash
  source /workspace/ai-builder/bin/launch-streamlit.sh
  ```

---
---

# License

This project is licensed under the terms of the [MIT License](https://github.com/AttuneEngineering/ai-builder/blob/main/LICENSE).

Happy Hacking!

---
---
