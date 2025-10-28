# 🧾 Data Extraction with Azure AI Foundry from multimodal content

*A practical demonstration of building a custom data extraction multimodel using the Azure AI Foundry Content Understanding service.*

---

## 🧩 Overview

This project demonstrates the end-to-end process of creating an AI-powered document extraction solution within **Azure AI Foundry**.
By leveraging the **Content Understanding** feature, this workflow shows how to build and test a custom analyzer capable of extracting structured data.

---

## 🎯 Objectives

* Connect securely to the **Azure AI Foundry** management center.
* Create a new **AI Hub resource** and a new **Project**.
* Initialize a **Content Understanding** task for "Invoice analysis".
* Clone or navigate to your project directory:
   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task10 - Extract information from multimodal content/Code"
   ```
* Define an extraction **schema** by uploading a sample file (`Data/invoice-1234.pdf`) and applying the "Invoice data extraction" template.
* Test the initial schema to verify field extraction and review confidence scores.
* Build and deploy a persistent **Content Understanding analyzer**.
* Test the deployed analyzer with a new, unseen invoice (`Data/invoice-1235.pdf`) to confirm its functionality.

---

## 🗂️ Workflow Steps

| Step                      | Description                                                                                                                                                                                                                |
| :------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1️⃣ Project Setup**     | A new project (`project55909396`) is created within a new AI Hub (`hub55989396`) in the Azure AI Foundry management center.                                                                                                |
| **2️⃣ Task Creation**     | The user navigates to `Content Understanding` and creates a "Create a new task" named "Invoice analysis" using "Standard mode - Single file analysis".                                                                     |
| **3️⃣ Schema Definition** | In the `Define schema` tab, a test file (`invoice-1234.pdf`) is uploaded, and the `Invoice data extraction` template is selected to pre-populate fields.                                                                   |
| **4️⃣ Initial Test**      | The `Test analyzer` tab is used to `Run analysis` on the sample file. The results show extracted fields like `AmountDue` (82.62) and `CustomerName` (John Smith).                                                          |
| **5️⃣ Build Analyzer**    | From the `Analyzer list` tab, a new `Content Understanding analyzer` is built with the name `invoice-analyzer`. The analyzer status shows "Ready".                                                                         |
| **6️⃣ Final Test**        | The built `invoice-analyzer` is tested by uploading a *different* file (`invoice-1235.pdf`) and running the analysis. This confirms it correctly extracts new data (e.g., `AmountDue`: 115.62, `CustomerName`: Ava Jones). |

---

## ⚙️ Core Components

* AI Hub Resource
* Content Understanding service
* Sample documents (e.g., `Data/invoice-1234.pdf`, `Data/invoice-1235.pdf`)

---

## ⚙️ Azure & Input Data URL's

   ```bash
https://ai.azure.com
https://ai.azure.com/managementCenter/allResources
https://github.com/microsoftlearning/mslearn-ai-information-extraction/raw/main/Labfiles/content/content.zip
   ```
---

## 🚀 Workflow Summary

1. **Create Project:** Start in the Azure AI Foundry Management center to create a new AI Hub resource and a new project.
2. **Define Task:** Navigate to Content Understanding and create a new "Invoice analysis" task.
3. **Define Schema:** Upload a sample invoice and select the "Invoice data extraction" template to define the fields to extract, such as `AmountDue`, `CustomerName`, and `InvoiceId`.
4. **Test & Build:** Use the "Test analyzer" to "Run analysis" on your sample. Once satisfied with the results, "Build" a persistent analyzer from the "Analyzer list" tab.
5. **Use Analyzer:** Test the "Ready" analyzer with new invoices to get structured data output.

---

## 🧠 Learning Outcomes

After completing this exercise, you will be able to:

* Navigate the Azure AI Foundry interface to create new AI projects.
* Configure a "Content Understanding" task for a specific document type like invoices.
* Understand the process of defining a data extraction schema using a template.
* Test, and deploy a document analyzer.
* Validate the analyzer's performance by testing it with new, unseen documents.

---

## 💡 Highlights

* 🤖 Uses a **pre-built "Invoice" template** to accelerate schema definition.
* 📊 Provides **confidence scores** for each extracted field (e.g., 89.20%, 94.90%, 99.10%).
* 🔁 Creates a **reusable analyzer** (`invoice-analyzer`) that can be called for new invoices.
* 🖱️ Provides a **low-code/no-code user interface** for building a custom document processing model.
* 🔁 Similarly, we can follow the similar steps for Slide Analysis, Voicemail Analysis, Conference call video Analysis as well.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---
