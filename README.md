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
  <a href="https://www.gnu.org/licenses/gpl-3.0">
      <img src="https://img.shields.io/badge/license-GPL%20v3-blue.svg" alt="License" />
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

>“Intelligence is the art in the eye of the beholder. How do you now that I am not a cyborg? How do I know that you are not a cyborg? The answer is we Turing test each other unconsciously at sufficient depth to satisfy ourselves. It becomes moot, or it is becoming moot.”
>
>~ Terence McKenna

---

### Abstract

The `AI Builder` repository is a template from which you can engineer your own application with open source generative AI. This codebase forms the cornerstone of Attune Engineering's [collection of private repositories](https://attuneengineering.com/source-code.html) for designing software architectures with Large Language Models. 

Within this repository you'll find:
  * **Server templates** for renting <a href="https://runpod.io?ref=zdeyr0zx" target="_blank">Runpod</a> GPU servers and serving open-source LLMs;
  * **Inference scripts** for communicating with your API endpoints and integrating your models into your software;
  * **DevOps configurations** for managing development environments and workflow automations with Docker and Gitpod;
  * **Multimodal vision** for unlocking open source image comprehension as an open alternative to GPT-4-Vision;
  * **LLM comparisons** to perform side-by-side inference across the suite of open source options and GPT-4.

This toolkit-based approach to interfacing with LLMs makes it easier to build complex architectures around your own fine-tuned open source LLMs. While OpenAI's API will continue to be the cheapest option for most all use cases - _because_ they can serve hundreds of thousands of people and amortise costs over concurrent requests - there are a few reasons why you may want to consider deploying your own API... if you
  * Cannot send data to OpenAI for privacy reasons;  _or_
  * Have a custom fine-tuned model you'd like to work with; _or_
  * Intend to build an application that can scale without being limited by OpenAI's API; _or_
  * You are passionate about decentralization democratization of AI systems...

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
    <li>Includes Mixtral 8x7B, LLaVA Vision, and a plethora of others...</li>
    <li>Find a README for each server template in <code>server-docs/</code>.</li>
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
    docker run -it --rm -p 8888:8888 $REGISTRY_IMAGE:main
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
Check out `dev.ipynb` to get started. To see further documentation about the Python source code contained within the instantiated `AIBuilder` class, see `src/README.md`.

---
---

# License

This project is licensed under the terms of the [GNU General Public License](https://github.com/AttuneEngineering/ai-builder/blob/main/LICENSE). This license is designed to ensure that software remains free and open, allowing users to run, study, share, and modify the software while allowing provisions for source-code that is sold for a fee. The license is clear that the definition of _**free**_ is free to use once accessed, not explicitly free to access.

This means that once you have purchased any code from Attune Engineering, you are free to do with it as you wish - be it share or modify. The stipulation to this, however, is that all forthcoming versions of the software must also be made available as complete source code with an accompyaning GPL license for all downstream applications. The aim of this license is not to prohibit the sale of derivative works, but rather to ensure free and open access to the source code provided under the _GPL-3_ license.

The rights granted to you as a purchaser of Attune Engineering's gated source code (or that which has been made available as open source) are as follows:

- **Freedom to Run**: The license grants users the freedom to run the program for any purpose.
- **Freedom to Modify**: Users can modify the software or any portion of it, thus allowing for the creation of derivatives that must also be licensed under GPL-3.
- **Freedom to Distribute**: Users can distribute copies of the original software to others, with or without modifications, under the same GPL-3 license terms - _See Discord for community stipulations_.
- **Source Code**: The license requires that all distributed software, including modifications and derived works, must be made available in source code form.
- **Patent Rights**: GPL-3 includes an express grant of patent rights from contributors to users, protecting users from patent litigation.
- **Tivoization**: GPL-3 addresses "Tivoization", ensuring that if the software is used in consumer products, users can still modify the software on those devices.
- **Compatibility with Other Licenses**: GPL-3 provides certain provisions for combining or linking with code under certain other licenses.

### Author's Note:

Attune Engineering is committed to distributing and supporting free and open source software development. If we envision a future where both the LLMs and the accompanying software architectures are democratized and open source, it's best to start building that vision now.

> "Popularity is tempting, and it is easy for a library developer to rationalize the idea that boosting the popularity of that one library is what the community needs above all...
>
> But we should not listen to these temptations, because we can achieve much more if we stand together. We free software developers should support one another. By releasing libraries that are limited to free software only, we can help each other's free software packages outdo the proprietary counterparts. The whole free software movement will have more popularity, because free software as a whole will stack up better against the competition."
- _[Why you shouldn't use the Lesser GPL for your next library](https://www.gnu.org/licenses/why-not-lgpl.html)_

Happy Hacking!

---
---
