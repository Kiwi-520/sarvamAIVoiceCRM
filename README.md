# 🎙️ AI Call Analytics Dashboard

An end-to-end B2B data pipeline that converts raw, multilingual customer support audio into structured, actionable business insights. Powered by **Sarvam AI** and **Streamlit**.

## 📌 The Problem
Sales and customer support teams in India operate heavily via voice notes and phone calls that mix English, Hindi, and regional languages. This creates a "black hole" of unstructured data. Managers cannot easily track sentiment, identify recurring issues, or monitor agent performance without listening to hours of audio manually.

## 💡 The Solution
This dashboard acts as a digital Call Quality Assurance (QA) manager. It provides a lightweight web interface where users can upload call recordings. The pipeline automatically:
1. Translates code-mixed audio into English.
2. Diarizes the transcript (separates Customer vs. Agent).
3. Analyzes the call for sentiment, satisfaction, and resolution.
4. Generates a 2-3 word structured Executive Summary ready for CRM ingestion.

## ⚙️ Features
* **Drag-and-Drop UI:** Built with Streamlit for frictionless file uploading (MP3/WAV/M4A).
* **Code-Mixed Translation:** Leverages Sarvam AI's `saaras:v3` model to handle Indian regional languages natively.
* **Intelligent Interrogation:** Uses Sarvam's `sarvam-30b` LLM to answer 9 specific business questions about the call (Issue, Satisfaction, Competitor Mentions, etc.).
* **Auto-Cleanup:** Implements Python's `tempfile` and `os` libraries to ensure heavy audio files are deleted from the server immediately after processing.

## 🛠️ Tech Stack
* **Frontend:** Streamlit
* **AI/Audio Engine:** Sarvam AI Python SDK
* **Backend/Logic:** Python 3, `python-dotenv`

## 🚀 Quick Start

**1. Clone the repository**
```bash
git clone [https://github.com/your-username/call-analytics-dashboard.git](https://github.com/your-username/call-analytics-dashboard.git)
cd call-analytics-dashboard