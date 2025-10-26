# 🧠 Text Classification with Azure AI

*A practical project using Azure Cognitive Services for custom text classification*

---

## 🧩 Overview

This script — **classify-text.py** — demonstrates how to use **Azure AI Language Service** to perform **custom text classification**.
It connects to a deployed custom text classification model in Azure and automatically classifies a batch of text documents into predefined categories.

---

## 🎯 Objectives

* Connect securely to Azure AI Text Analytics using endpoint and key credentials.
* Load a **custom text classification project** and deployment.
* Read and classify multiple text files from a folder.
* Display each file’s predicted **category** and its **confidence score**.
* Handle and report classification errors gracefully.

---

## 🗂️ Script Structure

| Section                       | Description                                                                   |
| ----------------------------- | ----------------------------------------------------------------------------- |
| **1️⃣ Configuration Setup**   | Loads Azure AI credentials, project, and deployment names from a `.env` file. |
| **2️⃣ Client Initialization** | Creates a `TextAnalyticsClient` using the Azure endpoint and API key.         |
| **3️⃣ Text File Loading**     | Reads all text files inside the `articles/` folder.                           |
| **4️⃣ Custom Classification** | Calls `begin_single_label_classify()` to classify each document.              |
| **5️⃣ Results Display**       | Prints each document’s classification label and confidence score.             |
| **6️⃣ Error Handling**        | Catches exceptions and reports API or I/O errors clearly.                     |

---

## ⚙️ Requirements

Ensure the following packages are installed:

```bash
python >= 3.8
azure-ai-textanalytics = 5.3.0
python-dotenv
```

To install dependencies:

```bash
pip install -r requirements.txt azure-ai-textanalytics==5.3.0
```

Input Data and Azure URL:

```bash
https://aka.ms/classification-articles
https://language.cognitive.azure.com/
```

You will also need an **Azure AI Language Service resource** with a **custom text classification project** deployed.
Set the following environment variables in a `.env` file:

```bash
AI_SERVICE_ENDPOINT = "<your_endpoint>"
AI_SERVICE_KEY = "<your_key>"
PROJECT = "<your_project_name>"
DEPLOYMENT = "<your_deployment_name>"
```

---

## 🚀 Getting Started

1. **Clone this repository**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task2 - Classify text/Code"
   ```

2. **Add your `.env` file** containing your Azure credentials and project info.

3. **Prepare your input files**

   * Create a folder named `articles/` in the same directory.
   * Add `.txt` files you want to classify.

4. **Run the script**

   ```bash
   python classify-text.py
   ```

5. **View results** in the terminal — each document’s predicted class and confidence score will be displayed.

---

## 🧠 Learning Outcomes

After completing this task, you will be able to:

* Connect and authenticate with Azure Cognitive Services.
* Utilize a **custom text classification model** in the Azure AI Language Service.
* Automate large-scale document classification using Azure SDKs.
* Interpret confidence scores to evaluate classification reliability.

---

## 💡 Highlights

* ⚙️ Automates classification for multiple text files in batch.
* 🧩 Integrates seamlessly with Azure’s custom text classification service.
* 📂 Simple `.env` configuration for flexible setup.
* 📊 Produces clear and interpretable classification outputs.
* 💬 Extensible for multi-label or hierarchical classification workflows.

---

## 🪪 License

This project is released for educational and learning purposes.

---
