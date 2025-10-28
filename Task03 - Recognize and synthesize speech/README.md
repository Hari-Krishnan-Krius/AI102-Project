# 🕒 Speaking Clock with Azure AI

*A voice-interactive project using Azure Cognitive Services for Speech Recognition and Synthesis*

---

## 🧩 Overview

This script — **speaking-clock.py** — demonstrates how to use **Azure Cognitive Services Speech SDK** to create an interactive **voice-based clock assistant**.
The program listens to your spoken input through the microphone, understands your command, and responds by **speaking the current time aloud** using natural-sounding neural voices.

---

## 🎯 Objectives

* Connect to Azure Speech Services using API key and region credentials.
* Capture **spoken input** from the user via a microphone.
* Recognize and transcribe the spoken phrase using **speech-to-text**.
* Respond with **text-to-speech** synthesis using a neural voice.
* Provide a simple example of integrating speech recognition and synthesis.

---

## 🗂️ Script Structure

| Section                               | Description                                                              |
| ------------------------------------- | ------------------------------------------------------------------------ |
| **1️⃣ Configuration Setup**           | Loads Azure Speech credentials (`KEY`, `REGION`) from a `.env` file.     |
| **2️⃣ Speech Service Initialization** | Configures `SpeechConfig` to connect to Azure Cognitive Services.        |
| **3️⃣ Speech Recognition**            | Uses `SpeechRecognizer` to capture and transcribe spoken input.          |
| **4️⃣ Command Processing**            | Listens for the phrase **"what time is it?"** and triggers the response. |
| **5️⃣ Speech Synthesis**              | Uses `SpeechSynthesizer` to speak the current time using a neural voice. |
| **6️⃣ Error Handling**                | Gracefully manages failed recognitions or API errors.                    |

---

## ⚙️ Requirements

Ensure the following packages are installed:

```bash
python >= 3.8
azure-cognitiveservices-speech = 1.42.0
python-dotenv
```

To install dependencies:

```bash
pip install -r requirements.txt azure-cognitiveservices-speech==1.42.0
```

You will also need an **Azure Speech Service resource** with the following environment variables stored in a `.env` file:

```bash
KEY = "<your_speech_key>"
REGION = "<your_speech_region>"
```

---

## 🚀 Getting Started

1. **Clone this repository**

   ```bash
   git clone https://github.com/Hari-Krishnan-Krius/AI102-Project.git
   cd "AI102-Project/Task3 - Recognize and synthesize speech/Code"
   ```

2. **Add your `.env` file** containing your Azure Speech credentials.

3. **Set up your microphone and speakers**
   Ensure your device’s microphone and speaker permissions are enabled.

4. **Run the script**

   ```bash
   python speaking-clock.py
   ```

5. **Speak your command**
   When prompted with *“Speak now...”*, say:

   > “What time is it?”

6. **Listen to the response**
   The program will respond with the current time spoken in a natural voice (e.g., *“The time is 10:45.”*).

---

## 🧠 Learning Outcomes

After completing this project, you will be able to:

* Use Azure Cognitive Services for both speech recognition and synthesis.
* Capture and interpret live voice input with Python.
* Convert text responses into spoken output using neural TTS models.
* Build foundational components for **voice-interactive AI applications**.

---

## 💡 Highlights

* 🎤 Real-time speech recognition and text-to-speech synthesis.
* ⚙️ Fully automated voice-based interaction loop.
* 🧩 Simple integration with Azure Speech SDK.
* 🗣️ Uses realistic **neural voice** (e.g., `en-GB-RyanNeural`).
* ⏰ Demonstrates real-time time reporting using Python’s `datetime`.

---

## 🪪 License

This project is released for educational and learning purposes.

---
