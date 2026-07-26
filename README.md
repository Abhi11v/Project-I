# RxVision AI 🩺👁️

> **Multimodal Prescription Decoder & Voice-Guided Drug Safety Agent**

> *A college lab assignment project bridging Computer Vision, NLP, and Voice AI to improve health literacy and prevent medication errors.*

---

## 📌 Problem Statement

Handwritten doctor prescriptions are notoriously difficult for patients to read. Misinterpreting dosage instructions or combining conflicting medications leads to thousands of preventable medical errors every year—disproportionately affecting elderly individuals and patients with low health literacy.

**RxVision AI** solves this by converting handwritten medical prescriptions into clear, structured text, checking for dangerous drug interactions in real time, and delivering multilingual audio instructions.

---

## ✨ Key Features

* 📷 **Handwritten OCR Parsing:** Extracts drug names, dosages, and daily schedules using pre-trained Vision-Language models.
* ⚠️ **Drug Interaction Checker:** Automatically queries official health APIs (RxNorm / openFDA) to flag dangerous drug-drug interactions.
* 🔊 **Multilingual Voice Summarization:** Translates complex medical terms into simple audio instructions in local languages using Text-to-Speech (TTS).
* 📅 **Automated Schedule Generator:** Formats parsed times into a clear daily routine table for patients.

---

## 🏗️ System Architecture

```
[ Prescription Image ] 
         │
         ▼
[ OpenCV Preprocessing ] ────► (Image Enhancement & Denoising)
         │
         ▼
[ Vision VLM / OCR ]    ────► (Extracts Medicine Names & Dosages)
         │
         ▼
[ RxNorm / openFDA API ] ───► (Checks Drug Interactions & Warnings)
         │
         ▼
[ Text-to-Speech (TTS) ] ───► (Generates Spoken Patient Instructions)
         │
         ▼
[ Streamlit Web UI ]    ────► (Displays Interactive Summary & Audio)
```

---

## 🛠️ Tech Stack

| Domain | Technology / Library |
| :--- | :--- |
| **Frontend UI** | Streamlit |
| **Image Processing** | OpenCV, PIL |
| **Vision & OCR** | Hugging Face Transformers (`microsoft/trocr-base-handwritten` / `Florence-2`) |
| **Drug Database APIs** | RxNav / RxNorm API, openFDA API |
| **Language & Voice** | `gTTS`, `deep-translator` |
| **Language** | Python 3.10+ |

---

## 📂 Project Structure

```text
RxVision-AI/
├── assets/                  # Sample prescription images and demo screenshots
├── src/
│   ├── ocr_engine.py        # Preprocessing & Vision OCR inference
│   ├── safety_agent.py      # RxNorm/openFDA API integrations
│   └── tts_engine.py        # Voice translation & audio synthesis
├── app.py                   # Main Streamlit web application
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/RxVision-AI.git](https://github.com/your-username/RxVision-AI.git)
cd RxVision-AI
```

### 2. Set Up Virtual Environment
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Application
```bash
streamlit run app.py
```

---

## 📊 Datasets & Resources

* **Kaggle:** [Handwritten Medical Prescriptions Collection](https://www.kaggle.com/)
* **Hugging Face:** `MMMuzammil/Medical_Prescription_Handwritten_Words`
* **Medical APIs:** [NIH RxNorm REST API](https://rxnav.nlm.nih.gov/) & [openFDA API](https://open.fda.gov/)

---

## 🤝 Contributing & License

This project is created for educational and academic submission purposes. Licensed under the [MIT License](LICENSE).
