# 🎧 Audio Chat with Azure AI

*A hands-on project demonstrating audio-to-text conversational AI using Azure OpenAI via AI Project Client.*

---

## 🧩 Overview

This script — **`audio-chat.py`** — showcases how to use **Azure AI Projects** and the **OpenAI Chat Completions API** to interact with an AI assistant using **audio inputs**.
The program encodes an audio file (in `.mp3` format), sends it to the Azure OpenAI model, and receives a conversational text response.

---

## 🎯 Objectives

* Connect securely to an Azure AI Project using the **AI Project Client**.
* Send **audio data** along with **text prompts** to an OpenAI chat model.
* Demonstrate how to handle **audio encoding (Base64)** for API compatibility.
* Enable user-driven, interactive question–answer sessions.
* Manage API responses and handle potential errors gracefully.

---

## 🗂️ Script Structure

| Section                             | Description                                                                                                    |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **1️⃣ Configuration Setup**         | Loads environment variables (`PROJECT_ENDPOINT`, `MODEL_DEPLOYMENT`) from a `.env` file using `python-dotenv`. |
| **2️⃣ Azure Client Initialization** | Creates an authenticated `AIProjectClient` using `DefaultAzureCredential` and retrieves an OpenAI client.      |
| **3️⃣ User Interaction Loop**       | Accepts user questions via terminal until `'quit'` is entered.                                                 |
| **4️⃣ Audio Encoding**              | Downloads and encodes an example `.mp3` file (`avocados.mp3`) from GitHub into Base64 format.                  |
| **5️⃣ Chat Completion Request**     | Sends the user’s text prompt and the encoded audio to the OpenAI model for a response.                         |
| **6️⃣ Output Handling**             | Prints the model’s text-based reply in the console.                                                            |
| **7️⃣ Error Handling**              | Catches and reports runtime or API-related exceptions.                                                         |

---

## ⚙️ Requirements

Ensure the following dependencies are installed:

```bash
python >= 3.9
azure-ai-projects
azure-identity
requests
python-dotenv
```

To install them:

```bash
pip install -r requirements.txt azure-identity azure-ai-projects openai
```
Azure URL:

```bash
https://ai.azure.com/
```

### 🔑 Environment Variables

Create a `.env` file in the same directory as your script with the following keys:

```bash
PROJECT_ENDPOINT = "<your_azure_ai_project_endpoint>"
MODEL_DEPLOYMENT = "<your_model_deployment_name>"
```

These correspond to your Azure AI Project’s endpoint and the deployed OpenAI model (e.g., `Phi-4-multimodal-instruct`).

---

## 🚀 Getting Started

1. **Clone the repository (or place the script in your workspace)**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task4 - Develop an audio-enabled chat app/Code"
   ```

2. **Set up your `.env` file**
   Include your `PROJECT_ENDPOINT` and `MODEL_DEPLOYMENT` values.

3. **Run the script**

   ```bash
   python audio-chat.py
   ```

4. **Interact with the model**

   * Type a question related to the audio (e.g., *“What is this audio about?”*).
   * The AI assistant will analyze the audio file and respond.
   * Type `quit` to exit the session.

---

## 🧠 Learning Outcomes

After completing this task, you will understand how to:

* Use **Azure AI Projects** to manage OpenAI-powered applications.
* Handle **audio inputs** in conversational models.
* Encode and transmit binary data via **Base64** for API calls.
* Create **interactive AI assistants** capable of multimodal input.

---

## 💡 Highlights

* 🔊 Combines text and audio inputs in a single chat interaction.
* ⚙️ Uses secure, managed credentials via Azure Identity.
* 🧩 Demonstrates a practical Azure OpenAI integration.
* 🧠 Provides reusable structure for multimodal AI pipelines.
* 💬 Fully interactive CLI-based conversation loop.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---
