# 💬 AI Chat Application with Azure OpenAI and Vision

*A practical project demonstrating how to build a multimodal chat assistant using Azure OpenAI and Azure AI Project services.*

---

## 🧩 Overview

This script — **`chat-app.py`** — demonstrates how to use **Azure OpenAI** through the **Azure AI Project SDK** to create a conversational assistant capable of analyzing **text and image inputs**.
It simulates an **AI assistant in a grocery store** that can answer questions about fruits, combining natural language understanding with visual reasoning.

---

## 🎯 Objectives

* Connect securely to **Azure AI Project** using **Azure Identity credentials**.
* Initialize an **Azure OpenAI client** within an AI Project environment.
* Accept **user prompts** interactively via the console.
* Process both **text and image** inputs in chat completions.
* Generate context-aware responses about produce or grocery items.
* Handle user input and exceptions gracefully.

---

## 🗂️ Script Structure

| Section                         | Description                                                                                         |
| ------------------------------- | --------------------------------------------------------------------------------------------------- |
| **1️⃣ Configuration Setup**     | Loads Azure connection settings from `.env` file.                                                   |
| **2️⃣ Client Initialization**   | Authenticates an `AIProjectClient` using `DefaultAzureCredential` and retrieves an `OpenAI` client. |
| **3️⃣ System Prompt Setup**     | Defines the assistant’s role — a knowledgeable AI in a grocery store that sells fruit.              |
| **4️⃣ Interactive Loop**        | Repeatedly accepts user questions until the user types `quit`.                                      |
| **5️⃣ Image Input Handling**    | Reads and encodes an image (`mystery-fruit.jpeg`) in base64 format for model input.                 |
| **6️⃣ Chat Completion Request** | Sends a multimodal request (text + image) to Azure OpenAI and prints the model’s response.          |
| **7️⃣ Error Handling**          | Catches and displays errors related to credentials, file access, or API calls.                      |

---

## ⚙️ Requirements

Ensure the following Python packages are installed:

```bash
python >= 3.9
azure-ai-projects
azure-identity
openai
python-dotenv
```

Install dependencies:

```bash
pip install -r requirements.txt azure-identity azure-ai-projects openai
```

Azure and Input data URL's:

```bash
https://ai.azure.com
https://github.com/MicrosoftLearning/mslearn-ai-vision/raw/refs/heads/main/Labfiles/gen-ai-vision/mango.jpeg
```
---

### 🔑 Environment Variables

Create a `.env` file in the same directory as your script containing the following credentials:

```bash
PROJECT_CONNECTION = "<your_azure_ai_project_endpoint>"
MODEL_DEPLOYMENT = "<your_azure_openai_model_deployment>"
```

These values correspond to your **Azure AI Project** configuration and **OpenAI model deployment** (e.g., gpt-4o) in the Azure portal.

---

## 🚀 Getting Started

1. **Clone or navigate to your project directory:**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task9 - Develop a vision-enabled chat app/Code"
   ```

2. **Add your `.env` file** with your project endpoint and model deployment details.

3. **Place an image file** named `mystery-fruit.jpeg` in the same directory as the script.

4. **Run the chat application:**

   ```bash
   az login
   python chat-app.py
   ```

5. **Ask questions interactively:**

   ```
   Ask a question about the image
   (or type 'quit' to exit)
   > What kind of fruit is this?
   ```

   The AI assistant analyzes the image and provides a detailed answer about the fruit shown.

---

## 🧠 Learning Outcomes

After completing this exercise, you will be able to:

* Connect and authenticate with **Azure AI Project** and **Azure OpenAI** services.
* Use **multimodal prompts** (text + image) to get intelligent responses.
* Integrate **computer vision** and **natural language processing** in conversational applications.
* Build and run **interactive AI-powered chat interfaces** in Python.

---

## 💡 Highlights

* 🖼️ Supports **image understanding** and **text-based conversation**.
* 💬 Provides interactive **real-time responses** in the terminal.
* 🔐 Uses **secure credentials** via `.env` and `DefaultAzureCredential`.
* 🧩 Clean, modular design for easy customization and reuse.
* ⚙️ Demonstrates **real-world integration** of Azure OpenAI within AI Projects.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---
