# 🧠 Image Classification with Azure Custom Vision

*A complete project demonstrating how to train and test a custom image classification model using Azure Custom Vision services.*

---

## 🧩 Overview

This project — combining **`train-classifier.py`** and **`test-classifier.py`** — shows how to use **Azure Custom Vision** to build, train, and test an image classification model.
It walks through **uploading and tagging training images**, **training a model**, and **classifying new test images** based on the trained model.

---

## 🎯 Objectives

* Connect securely to Azure Custom Vision using endpoint and key credentials.
* Upload and tag training images in an existing Custom Vision project.
* Train a new iteration of a classification model programmatically.
* Classify unseen test images using the trained model.
* Display classification results with confidence percentages.
* Handle environment setup and exceptions gracefully.

---

## 🗂️ Project Structure

| File                        | Description                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------- |
| **`train-classifier.py`**   | Uploads and tags training images, and trains a new Custom Vision model iteration.                 |
| **`test-classifier.py`**    | Uses the trained model to classify new test images and prints predictions with confidence scores. |
| **`.env`**                  | Stores API keys, endpoints, and project configuration details securely.                           |
| **`training-images/`** | Folder containing training images organized by tag name.                                          |
| **`test-images/`**          | Folder containing images to test model predictions.                                               |

---

## ⚙️ Requirements

Ensure the following Python packages are installed:

```bash
python >= 3.9
azure-cognitiveservices-vision-customvision
python-dotenv
```

Install dependencies:

```bash
pip install -r requirements.txt azure-cognitiveservices-vision-customvision
```

Azure & Data Source URL's:

```bash
https://customvision.ai
https://github.com/MicrosoftLearning/mslearn-ai-vision/raw/main/Labfiles/image-classification/training-images.zip
https://aka.ms/test-apple
```

### 🔑 Environment Variables

Update the `.env` files in the same directory as your scripts containing the following credentials:

```bash
TrainingEndpoint = "<your_custom_vision_training_endpoint>"
TrainingKey = "<your_custom_vision_training_key>"
PredictionEndpoint = "<your_custom_vision_prediction_endpoint>"
PredictionKey = "<your_custom_vision_prediction_key>"
ProjectID = "<your_custom_vision_project_id>"
ModelName = "<your_model_name>"
```

These values correspond to your **Azure Custom Vision resource** in the Azure portal.

---

## 🚀 Getting Started

### 🧰 1. Train the Model

Run the training script to upload images and train your classifier:

```bash
python train-classifier.py
```

**Process overview:**

* Uploads tagged images from `Data/training-images/`.
* Initiates a new training iteration.
* Monitors training progress until completion.
* Prints `"Model trained!"` when finished.

---

### 🧪 2. Test the Model

After training, run the test script to classify unseen images:

```bash
python test-classifier.py
```

**Process overview:**

* Loads test images from `Data/test-images/`.
* Uses the trained model to predict image labels.
* Prints classification results in the console (for example):

```
IMG_TEST_1.jpg : apple (100%)
IMG_TEST_2.jpg : banana (100%)
IMG_TEST_3.jpg : orange (100%)
```

Only predictions above **50% confidence** are displayed.

---

## 🧠 Learning Outcomes

After completing this project, you will be able to:

* Connect and authenticate with **Azure Custom Vision APIs** using Python.
* Programmatically **train image classifiers** and **test predictions**.
* Manage **image uploads**, **tags**, and **model iterations**.
* Automate the end-to-end **machine learning workflow** for image classification.
* Understand how confidence scores indicate model prediction strength.

---

## 💡 Highlights

* 🤖 End-to-end automation for **training and testing** an image classifier.
* 🧩 Modular scripts for **reusability** and **maintainability**.
* ⚙️ Secure configuration via environment variables.
* 📊 Outputs clear prediction results with confidence percentages.
* 💬 Practical demonstration of **Azure Cognitive Services Custom Vision**.

---

## 🪪 License

This project is intended for **educational and learning purposes**.

---
