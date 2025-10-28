# 📝 Read Text from Images with Azure AI Vision

*A hands-on project demonstrating how to extract and annotate text from images using Azure AI Vision services.*

---

## 🧩 Overview

This script — **`read-text.py`** — showcases how to use **Azure AI Vision** to detect and read printed text within images.
It extracts **lines and words**, displays their confidence scores, and generates **annotated images** highlighting detected text regions.

---

## 🎯 Objectives

* Connect securely to Azure AI Vision using endpoint and key credentials.
* Analyze images for **text recognition (OCR)** using the `READ` visual feature.
* Extract detected **lines** and **individual words** from images.
* Annotate and save images with **bounding boxes** drawn around recognized text.
* Handle user-specified image inputs via command-line arguments.
* Gracefully manage errors during API calls or file operations.

---

## 🗂️ Script Structure

| Section                       | Description                                                                                                                |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **1️⃣ Configuration Setup**   | Loads Azure Vision endpoint and key from a `.env` file using `python-dotenv`.                                              |
| **2️⃣ Client Initialization** | Creates an authenticated `ImageAnalysisClient` using `AzureKeyCredential`.                                                 |
| **3️⃣ Image Input Handling**  | Reads a default image (`images/Lincoln.jpg`) or a user-specified file passed as a command-line argument.                   |
| **4️⃣ Text Extraction**       | Calls the Azure Vision API with the `VisualFeatures.READ` parameter to perform OCR.                                        |
| **5️⃣ Results Display**       | Prints detected lines and words along with their confidence scores.                                                        |
| **6️⃣ Visualization**         | Draws bounding polygons around detected lines and words using `PIL` and saves annotated images (`lines.jpg`, `words.jpg`). |
| **7️⃣ Error Handling**        | Catches and reports exceptions for API or file-related issues.                                                             |

---

## ⚙️ Requirements

Ensure the following Python packages are installed:

```bash
python >= 3.9
azure-ai-vision-imageanalysis == 1.0.0
python-dotenv
Pillow
matplotlib
```

Install dependencies:

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

These correspond to your **Azure AI Vision resource** credentials in the Azure portal.

---

## 🚀 Getting Started

1. **Clone or navigate to your project directory:**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task6 - Read text in images/Code"
   ```

2. **Add your `.env` file** containing your Vision endpoint and key.

3. **Prepare input images**

   * Default input file: `Data/images/Lincoln.jpg`
   * To analyze a different image, specify it as a command-line argument:

     ```bash
     python read-text.py Data/images/Lincoln.jpg
     ```

4. **Run the script**

   ```bash
   python read-text.py
   ```

5. **View results**

   * The console displays detected **lines of text** and **individual words** with confidence values.
   * Annotated output images — `lines.jpg` and `words.jpg` — are saved in the working directory.

---

## 🧠 Learning Outcomes

After completing this exercise, you will be able to:

* Use **Azure AI Vision** to perform **OCR (Optical Character Recognition)** on images.
* Extract and visualize recognized **text elements** with bounding boxes.
* Configure and authenticate API calls securely with environment variables.
* Handle API responses and exceptions effectively in Python.

---

## 💡 Highlights

* 🧾 Detects printed text and separates lines from words.
* ✍️ Generates annotated images for visual confirmation.
* 🔐 Secure authentication through `.env` configuration.
* 🧩 Modular, easy-to-extend structure for future enhancements.
* ⚙️ Practical demonstration of **Azure Cognitive Services for OCR**.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---
