# Running OpenWebUI on QuickPod  

### OpenWebUI - The Easiest Local LLM Experience

**Last updated:** September 9, 2025

> [!NOTE]
> To skip to the **Guide**, go **[Further down This Page](https://github.com/quickpod/OpenWebUI?tab=readme-ov-file#guide).**

---
# Introduction

I've tried several Local LLM Clients, always with the goal of getting the same polished experience and useful features as a modern online chatbot service. That's a pretty high bar, which is why I've never found a full offline replacement. That is, until I found OpenWebUI and made it a template. It's feature-packed rivaling the leading major LLM's, including deep thinking, image processing, and Web Search (which has to be enabled in Settings). It also offers a large pool of diverse models, including Google Gemma, Meta Llama, Qwen, Deepseek, and many more. And of course it's all offline, which means no rate limits. 

### Although I wasn't able to use it, I think the accounts feature could be useful for some wanting to scale local AI while using one server.

This has an account function, which means multiple users can generate on the same instance with different chats, models, settings, etc. Multi-GPU is utilized very well for this and gives a great experience. As long as it's using different models, GPUs can generate independently.

---
# Guide

> [!NOTE]
> Although it's not reccomended, Ollama supports running CPU-Only without GPU Acceleration. Use this guide but just with the OpenWebUI-CPU template.


## Create Your Pod

1. Go to [QuickPod Templates](https://console.quickpod.io/templates)  
2. Find **`OpenWebUI`** and click **Select**.

   ![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/SelectButton.png?raw=true)

> [!NOTE]
> Ollama supports using multiple GPUs for large models although it's not recommended. It also supports using multiple models at the same time with different accounts, which is a feature that works very well.

3. Choose a machine:
   
   - **CPU:** Many Cores, High speed Memory important. Will often be slower than GPU assisted.
   - **GPU:** High speed VRAM is the most crucial part, although capacity also plays a role. For best results, I'd recommend: \
         RTX 5090, 32GB GDDR7 \
         RTX 4090, 24GB GDDR6X \
         RTX 3090, 24GB GDDR6X \
For lower parameter models, modern budget alternatives such as the **RTX 4060 TI** or **RTX 3060** will also work.

   ![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/RentExample.png?raw=true)

4. Click the **Connect** menu and **Open the First Port** (Port 8080).
   ![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/ConnectButton.png?raw=true)
   ![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/OpenPortButton.png?raw=true)

---

## Using OpenWebUI

> [!NOTE]
> *OpenWebUI* uses the **Ollama API** to connect to the models. Additional model and API information can be found on the **[Ollama Site](https://ollama.com).**

1. Make the Admin Credentials 

![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/LoginExample.png?raw=true)



> [!NOTE]
> All models with details can be found in the **[Ollama Model Collection](https://ollama.com/search).**

2: Download your First Model

- Go to the **Models Menu** on the left and type in any model from the **Ollama Model Collection.** 
- Click **Pull [Your-Model] From Ollama.com.** 
- **Wait** For it to download.

![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/ModelExample.png?raw=true)

3: Start Chatting!

![image](https://github.com/quickpod/OpenWebUI/blob/main/Photos/UseExample.png?raw=true)

---


> [!NOTE]
> The **Ollama API** has also been forwarded at internal **Port 11434** and is accessable outside the container by default from the *Second Port Forward Box*. Several WebUI's use Ollama, so this template can also be used as an Ollama base server.
