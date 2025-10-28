# 🧠 Text Analysis with Azure AI  
*A practical project using Azure Cognitive Services for Natural Language Processing (NLP)*

---

## 🧩 Overview  
This script — **text-analysis.py** — demonstrates how to use **Azure AI Language Service** to perform automated text analysis on a collection of text files.  
It extracts insights such as **language detection**, **sentiment analysis**, **key phrase extraction**, and **entity recognition** from text data, enabling intelligent document understanding and analytics.

---

## 🎯 Objectives  
- Connect to Azure AI Text Analytics using endpoint and key credentials.  
- Analyze multiple text files in a folder for NLP insights.  
- Detect the **language** of each document.  
- Determine **sentiment polarity** (positive, neutral, or negative).  
- Extract **key phrases** summarizing important topics.  
- Recognize **named entities** and **linked entities** with external references.

---

## 🗂️ Script Structure  
| Section | Description |
|----------|-------------|
| **1️⃣ Configuration Setup** | Loads Azure AI service credentials from a `.env` file. |
| **2️⃣ Client Initialization** | Creates a `TextAnalyticsClient` using the Azure endpoint and key. |
| **3️⃣ Text File Processing** | Iterates through the `reviews/` folder and reads text files. |
| **4️⃣ Language Detection** | Identifies the primary language for each file. |
| **5️⃣ Sentiment Analysis** | Determines if the tone is positive, negative, or neutral. |
| **6️⃣ Key Phrase Extraction** | Lists significant phrases that represent the document’s context. |
| **7️⃣ Entity Recognition** | Extracts and categorizes named entities (e.g., people, places, organizations). |
| **8️⃣ Linked Entity Recognition** | Finds entities linked to external resources like Wikipedia. |

---

## ⚙️ Requirements  
Ensure the following packages are installed:

```bash
python >= 3.8
azure-ai-textanalytics = 5.3.0
python-dotenv
````

To install dependencies:

```bash
pip install -r requirements.txt azure-ai-textanalytics==5.3.0
```

You will also need an **Azure AI Language Service resource** with the following environment variables stored in a `.env` file:

```bash
AI_SERVICE_ENDPOINT = "<your_endpoint>"
AI_SERVICE_KEY = "<your_key>"
```

---

## 🚀 Getting Started

1. **Clone this repository**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task1 - Analyze text/Code"
   ```

2. **Add your `.env` file** containing your Azure credentials.

3. **Prepare your input files**

   * Create a folder named `reviews/` in the same directory.
   * Add `.txt` files you want to analyze like given under `Data/` directory.

4. **Run the script**

   ```bash
   python text-analysis.py
   ```

5. **View results** in the terminal — including detected language, sentiment, key phrases, entities, and links.

---

## 🧠 Learning Outcomes

After completing this task, you will be able to:

* Connect and authenticate with Azure Cognitive Services.
* Perform real-world NLP tasks using prebuilt AI models.
* Automate language detection, sentiment analysis, and entity recognition.
* Understand how Azure’s Text Analytics API can be integrated into intelligent applications.

---

## 💡 Highlights

* ⚙️ Fully automated text analysis pipeline.
* 🧩 Uses Azure AI SDKs for high-level NLP capabilities.
* 📂 Processes multiple text files in batch mode.
* 🌍 Detects multilingual content seamlessly.
* 📊 Extracts meaningful insights for further analytics or visualization.

---

## 🪪 License

This project is released for educational and learning purposes.

---
