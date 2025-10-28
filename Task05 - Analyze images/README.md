# 🖼️ Image Analysis with Azure AI Vision

*A practical project demonstrating how to analyze and annotate images using Azure AI Vision services.*

---

## 🧩 Overview

This script — **`image-analysis.py`** — demonstrates how to use **Azure AI Vision** to analyze visual content in images.
It extracts **captions, tags, dense captions, objects, and people** from an image and generates **annotated output images** highlighting detected features.

---

## 🎯 Objectives

* Connect securely to Azure AI Vision using endpoint and key credentials.
* Analyze images for visual features such as **captions**, **tags**, **objects**, and **people**.
* Automatically **annotate images** with bounding boxes for detected objects and people.
* Handle user-specified image inputs from the command line.
* Manage API responses and handle errors gracefully.

---

## 🗂️ Script Structure

| Section                       | Description                                                                                                          |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **1️⃣ Configuration Setup**   | Loads Azure Vision endpoint and key from a `.env` file using `python-dotenv`.                                        |
| **2️⃣ Client Initialization** | Creates an authenticated `ImageAnalysisClient` using `AzureKeyCredential`.                                           |
| **3️⃣ Image Input Handling**  | Reads a default image (`images/street.jpg`) or a user-specified file passed as a command-line argument.              |
| **4️⃣ Image Analysis**        | Calls the Azure Vision API with multiple `VisualFeatures`: Caption, Dense Captions, Tags, Objects, and People.       |
| **5️⃣ Results Extraction**    | Prints detected captions, tags, objects, and people with confidence scores.                                          |
| **6️⃣ Visualization**         | Draws bounding boxes around objects and people using `PIL` and saves annotated images (`objects.jpg`, `people.jpg`). |
| **7️⃣ Error Handling**        | Catches and reports exceptions during API calls or file operations.                                                  |

---

## ⚙️ Requirements

Ensure the following Python packages are installed:

```bash
python >= 3.9
azure-ai-vision-imageanalysis = 1.0.0
python-dotenv
```

Install dependencies with:

```bash
pip install -r requirements.txt azure-ai-vision-imageanalysis==1.0.0
```

---

### 🔑 Environment Variables

Create a `.env` file in the same directory as your script containing the following credentials:

```bash
AI_SERVICE_ENDPOINT = "<your_azure_ai_vision_endpoint>"
AI_SERVICE_KEY = "<your_azure_ai_vision_key>"
```

These values correspond to your **Azure AI Vision resource** in the Azure portal.

---

## 🚀 Getting Started

1. **Clone this repository** (or move to your project directory):

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task5 - Analyze images/Code"
   ```

2. **Add your `.env` file** with your Vision endpoint and key.

3. **Prepare input images**

   * Default input file: `Data/street.jpg`
   * You can analyze a different image by specifying it as a command-line argument:

     ```bash
     python image-analysis.py Data/street.jpg
     ```

4. **Run the script**

   ```bash
   python image-analysis.py
   ```

5. **View results**

   * The console displays detected **captions**, **tags**, **objects**, and **people**.
   * Annotated output images — `objects.jpg` and `people.jpg` — are saved in the `Results/` directory.

---

## 🧠 Learning Outcomes

After completing this exercise, you will be able to:

* Connect and authenticate with **Azure AI Vision** using Python SDKs.
* Perform **comprehensive image analysis** with multiple visual features.
* **Visualize and annotate** objects and people detected in images.
* Implement error handling and flexible user input options.

---

## 💡 Highlights

* 🖼️ Detects multiple visual elements — captions, tags, objects, and people.
* ✍️ Generates annotated images for better visualization.
* ⚙️ Easily configurable through `.env` file credentials.
* 🧩 Modular code structure for extension and reuse.
* 💬 Demonstrates real-world integration of Azure Cognitive Services in Python.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---

