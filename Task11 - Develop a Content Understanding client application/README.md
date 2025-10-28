# 📸 Business Card Analysis with Azure AI

*A project using the Azure AI Content Understanding REST API to build and query a custom document analyzer.*

---

## 🧩 Overview

This project demonstrates how to use the **Azure AI Content Understanding** service (part of Azure AI Vision) via its REST API. It consists of two main scripts:

1. **`create-analyzer.py`**: Builds a custom analyzer in your Azure service based on the provided `biz-card.json` schema.
2. **`read-card.py`**: Uses that custom analyzer to scan an image of a business card and extract structured data (like Name, Title, Email, etc.).

---

## 🎯 Objectives

* Connect to an Azure AI service using its REST API, endpoint, and key.
* Define a custom schema for document extraction.
* Programmatically create a custom "analyzer" resource in the service.
* Submit an image (like a business card) for analysis to the custom analyzer.
* Handle asynchronous API operations by polling for results.
* Parse the structured JSON response to retrieve the extracted fields.

---

## 🗂️ Project Structure

| File / Script            | Description                                                                                                                                                    |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`biz-card.json`**      | A JSON schema defining the specific fields to extract from a business card (e.g., `Company`, `Name`, `Title`, `Email`, `Phone`).                               |
| **`create-analyzer.py`** | Connects to the Azure service, deletes any old analyzer with the same name, and creates a new one using the `biz-card.json` schema.                            |
| **`read-card.py`**       | Takes an image file as input and sends it to the analyzer created by the first script. It polls for the analysis results and then prints the extracted fields. |

---

## ⚙️ Requirements

Ensure the following packages are installed:

```bash
python >= 3.8
requests
python-dotenv
```

To install dependencies:

```bash
pip install -r requirements.txt
```
---
Azure & Data Source URL's:

```bash
https://ai.azure.com/
https://ai.azure.com/managementCenter/allResources
```
---
You will also need an **Azure AI Foundry project** (provisioned as an **AI hub resource**) which provides the **Content Understanding** service.
From your project's **Overview** page, you will need the credentials for **Azure AI Services** (Endpoint and Key) stored in a `.env` file:

```bash
# Your Azure AI Services endpoint
ENDPOINT="<your_endpoint>"

# Your Azure AI Services key
KEY="<your_key>"

# A name for your custom analyzer
ANALYZER_NAME="my-biz-card-analyzer"
```

---

## 🚀 Getting Started

1. **Clone this repository**:

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task11 - Develop a Content Understanding client application/Code"
   ```

2. **Add your `.env` file** containing your Azure `ENDPOINT`, `KEY`, and `ANALYZER_NAME`.

3. **Prepare your input file(s)**

   * Add business card images to the same directory (e.g., `Data/biz-card-1.png`, `Data/biz-card-2.png`).

4. **Run the *create* script** (you only need to do this once):

   ```bash
   python create-analyzer.py
   ```

   *Wait for the confirmation message: `Analyzer 'business-card-analyzer' created successfully.`*

5. **Run the *read* script** to analyze your image:

   ```bash
   # Analyze the first card
   python read-card.py biz-card-1.png
   ```
   ```bash
   # Analyze the second card
   python read-card.py biz-card-2.png
   ```

6. **View results** in the terminal. A full `Results/results.json` file will also be created with the complete API response.

---

## 🧠 Learning Outcomes

After completing this task, you will be able to:

* Authenticate with and control Azure AI services using the REST API.
* Define and deploy a custom document model for structured data extraction.
* Understand and manage asynchronous API operations (submit, poll, retrieve).
* Extract specific, named fields from an image using a custom model.

---

## 💡 Highlights

* ⚙️ Uses the raw **Azure REST API** (via `requests`) instead of the Python SDK.
* 🧩 Demonstrates a two-step process: **build** a custom model and **query** it.
* 📄 **Schema-driven extraction** for custom document types.
* 🔄 Handles **asynchronous polling** for long-running analysis jobs.
* 📤 Saves the complete JSON response for inspection and debugging.

---

## 🪪 License

This project is released for educational and learning purposes.

---
