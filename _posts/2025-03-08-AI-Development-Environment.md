---
layout:  post
title: "DOC: Installing Local AI Models"
date: 2025-03-08 12:04:17 -03:00
description: "Using Ollama, Open Web-UI, KokoroTTS, StableDiffusion and more models from Ollama to build a local AI environment for tests and tasks."
tags: [Local AI Models, Ollama, Open WebUI, KokoroTTS, Stable Diffusion, Text-to-Speech, Image Generation, Python, Web Search, Docker, Development Guide]
permalink: /posts/LocalAISetup  # Custom URL path (optional)
---

In this guide, we'll walk you through the process of setting up a local AI environment using various powerful tools and models. This includes using **Ollama** for model management, **Open Web-UI** for an intuitive interface, **KokoroTTS** for text-to-speech capabilities, and **Stable Diffusion** for image generation. These setups will allow you to test and run AI models locally, giving you full control over your environment for tasks and experiments.

Before diving into the setup process, please review the important security information below to ensure that your local environment remains secure.

## ⚠️ **Security Notice**  
This document provides steps to set up a local AI environment. **Do not share or expose sensitive information**, such as API keys, authentication tokens, or private data, in public repositories or forums.  

- **Environment Variables:** Always store API keys and credentials securely using `.env` files or system environment variables.  
- **Web Services & Ports:** If exposing services (e.g., Open WebUI, Docker containers), ensure proper firewall rules and authentication measures are in place.  
- **Google API Key & Engine ID:** Keep these confidential. Do not hardcode them in public code or documentation.  

**Use this guide responsibly and follow best security practices to protect your data and infrastructure.**


***

## 📂 Start Sources

### 🧑‍💻 Setting up a AI Dev Env
[Beginner’s Guide: Setting Up Your AI Development Environment with VSCode, GitHub, Cline & OpenRouter](https://youtu.be/6zo80iyLkjQ?list=PLI--os-5eUftg2UHFw7NO6R5PfEW9oHxM)

[Run Cline FREE! The Cline Hack Nobody's Talking About (Qwen2.5-coder-tools)](https://youtu.be/RXi0Cz0ibKY?list=PLI--os-5eUftg2UHFw7NO6R5PfEW9oHxM)
***

### 🤖 Setting up Open WebUI
[Ollama Environment Variables](https://www.restack.io/p/ollama-answer-environment-variables-cat-ai)
This PC -> Properties -> Advanced System Setting -> Environment Variables ->  New System Variables

| Variable name  |  Variable value    |
| -------------- | ------------------ |
|OLLAMA_MODELS   | path to the folder |

***
### 🐍 Installing and using Anaconda
[Anaconda.org](https://anaconda.org/)
`conda --version`  
`conda create --name env_p311 python=3.11` :: Create a **new environment** called env_p311 with Python 3.11  
`activate env_p311` :: **Activate** the environment  
`conda deactivate`  **Deactivate** the environment  
`conda remove --name env_p311 --all` :: **Removing** an environment  
`conda env list` :: List all environments  

***
### 🌐 Install Open WebUI
[Open WebUI GitHub](https://github.com/open-webui/open-webui)
Inside Conda Environment  
`pip install open-webui` :: Install Open WebUI  
`open-webui serve` :: Run Open WebUI Server  
Access: http://localhost:8080/  

***
### 👩‍🦲 Installing Models
[Ollama Models Library](https://ollama.com/library)
Choose a model  
Example: qwen2.5-coder:7b  
Open the Admin Panel in Open WebUI by clicking on the username in the bottom left-hand corner, navigate to Settings -> Models, Click the Down Arrow in the upper left-hand corner, insert the name of the model below the "Pull a model from Ollama.com", Click the Download button.

___
### ❣️ Installing Kokoro
[Tutorial how to install Kokoro](https://docs.openwebui.com/tutorials/text-to-speech/Kokoro-FastAPI-integration)
[Open WebUI: Kokoro TTS Setup Guide](https://youtu.be/UzpGgC2SmzI)
[Model Voices](https://huggingface.co/hexgrad/Kokoro-82M/blob/main/VOICES.md#british-english)
[Speech to Text Database](https://github.com/ggerganov/whisper.cpp)

`docker run --gpus all -p 8880:8880 ghcr.io/remsky/kokoro-fastapi-gpu`

___
### 🕸️ Enable Web Search 
[How to Enable Web Search in Open WebUI](https://youtu.be/fwscnJu_Md0)  
[Google PSE Engine Id](https://programmablesearchengine.google.com/controlpanel/all)  
[Google PSE API Key](https://developers.google.com/custom-search/v1/introduction)

Open the Admin Panel in Open WebUI by clicking on the username in the bottom left-hand corner, navigate to Settings -> Web Search, Allow Web Search and fill the respective fields

**Custom Search JSON API** provides **100 search** queries per day **for free**. If you need more, you may sign up for [billing](https://cloud.google.com/billing/docs/how-to/manage-billing-account) in the API Console. Additional requests cost $5 per 1000 queries, up to 10k queries per day.

***
### 🖼️ Installing Stable Diffusion
[Stable Diffusion web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui)
[ControlNet for Stable Diffusion WebUI](https://github.com/Mikubill/sd-webui-controlnet)
[ControlNet Install - Tutorial](https://stable-diffusion-art.com/controlnet/)
[Open WebUI with AUTOMATIC1111](https://docs.openwebui.com/tutorials/images/)
[Stable Diffusion Prompt Generator](https://ollama.com/brxce/stable-diffusion-prompt-generator)

`repeat it back:`

***