# 😊 Face Detection and Analysis with Azure AI Vision

*A practical project demonstrating how to detect and analyze human faces in images using Azure AI Vision Face services.*

---

## 🧩 Overview

This script — **`analyze-faces.py`** — shows how to use **Azure AI Vision (Face API)** to detect faces in an image and extract detailed **facial attributes**, such as **head pose**, **occlusion**, and **accessories**.
It also generates an **annotated image** with bounding boxes drawn around detected faces.

---

## 🎯 Objectives

* Connect securely to Azure AI Vision Face API using endpoint and key credentials.
* Detect human faces in images and retrieve **facial attributes** including head pose, occlusion, and accessories.
* Annotate detected faces visually in an image.
* Handle image input dynamically via command-line arguments.
* Manage API responses and exceptions effectively.

---

## 🗂️ Script Structure

| Section                       | Description                                                                                                  |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **1️⃣ Configuration Setup**   | Loads Azure Vision endpoint and key from a `.env` file using `python-dotenv`.                                |
| **2️⃣ Client Initialization** | Creates an authenticated `FaceClient` using `AzureKeyCredential`.                                            |
| **3️⃣ Image Input Handling**  | Reads a default image (`images/face1.jpg`) or a user-specified file passed via the command line.             |
| **4️⃣ Face Detection**        | Calls the Azure Vision Face API to detect faces and retrieve attributes (head pose, occlusion, accessories). |
| **5️⃣ Results Extraction**    | Prints detected facial attributes for each face, including yaw, pitch, roll, and accessories.                |
| **6️⃣ Visualization**         | Draws bounding boxes around detected faces and saves an annotated image (`detected_faces.jpg`).              |
| **7️⃣ Error Handling**        | Gracefully handles exceptions related to missing files, invalid credentials, or API errors.                  |

---

## ⚙️ Requirements

Ensure the following Python packages are installed:

```bash
python >= 3.9
azure-ai-vision-face == 1.0.0
python-dotenv
Pillow
matplotlib
```

Install dependencies:

```bash
pip install -r requirements.txt azure-ai-vision-face==1.0.0b2
```
---

### 🔑 Environment Variables

Create a `.env` file in the same directory as your script containing the following credentials:

```bash
AI_SERVICE_ENDPOINT = "<your_azure_face_api_endpoint>"
AI_SERVICE_KEY = "<your_azure_face_api_key>"
```

These correspond to your **Azure AI Vision (Face API)** resource credentials in the Azure portal.

---

## 🚀 Getting Started

1. **Clone or navigate to your project directory:**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task7 - Detect and analyze faces/Code"
   ```

2. **Add your `.env` file** with your endpoint and key.

3. **Prepare input images**

   * Default input file: `Data/images/face1.jpg`
   * To analyze a different image, specify it as a command-line argument:

     ```bash
     python analyze-faces.py Data/images/face1.jpg
     ```

4. **Run the script**

   ```bash
   python analyze-faces.py
   ```

5. **View results**

   * The console displays details about detected **faces** and their **attributes**.
   * An annotated output image — `detected_faces.jpg` — is saved in the working directory.

---

## 🧠 Learning Outcomes

After completing this exercise, you will be able to:

* Connect and authenticate with **Azure AI Vision Face API**.
* Perform **face detection and attribute extraction** on images.
* Understand key facial attributes such as **head pose**, **occlusion**, and **accessories**.
* **Visualize detected faces** through annotated output images.

---

## 💡 Highlights

* 👁️ Detects multiple faces in a single image.
* 📐 Extracts **head pose** and other useful facial attributes.
* ✍️ Generates annotated images for visual feedback.
* ⚙️ Secure and configurable using environment variables.
* 🧩 Modular, well-structured code — easy to extend and integrate.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---
