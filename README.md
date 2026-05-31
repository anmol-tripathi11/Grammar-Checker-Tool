# **🧠 Grammar Checker Tool**
ML-Powered Grammatical Error Detection & Correction System       

Internship Project @ TCS iON — Automate Detection and Recognition of Grammatical Errors | Dec 2024 – Mar 2025 | 125 Hours       

       
📌 Overview       
A full-stack NLP web application that automatically detects and corrects grammatical errors in English text. Built as part of a remote internship with TCS iON (Tata Consultancy Services), this project combines machine learning classifiers, rule-based linguistic pipelines, and LanguageTool integration to deliver contextual grammar correction at scale.       
Why this project matters:       

Bridges the gap between raw NLP research and a usable, deployed product       
Processes unstructured text through a structured ML inference pipeline              
Demonstrates end-to-end ownership — from dataset preparation to cloud deployment       

       
🎯 Problem Statement       
Automated grammar correction is a core NLP challenge with applications in education, content moderation, document processing, and BI reporting pipelines. This tool solves that by building a multi-layer error detection system that goes beyond simple spell-check — catching tense inconsistencies, subject-verb disagreement, modal verb errors, and more.       
       
✨ Key Features       
FeatureDescription🔍 Real-time Grammar CheckingInstant detection of grammatical errors as you type🤖 ML-Powered ClassificationScikit-learn models trained on Kaggle datasets for contextual error detection📊 Grammar ScoringQuantitative writing quality score (0–100) per submission🛠️ Multi-layer Error DetectionRule-based + ML + LanguageTool combined pipeline💡 Smart SuggestionsContext-aware corrections with severity ratings (low / medium / high)🌐 REST APIClean Flask API endpoints for integration into other systems☁️ Cloud DeployedLive on Hugging Face Spaces — accessible anywhere, no setup required       
       
🏗️ System Architecture       
User Input (Text)       
       │       
       ▼       
┌─────────────────────────────────────┐       
│          Frontend (HTML/CSS/JS)     │       
│     ┌──────────────────────────┐    │       
│     │   Fetch API → Flask API  │    │       
│     └──────────────────────────┘    │       
└─────────────────────────────────────┘              
       │       
       ▼       
┌─────────────────────────────────────┐       
│         Flask Backend (app.py)      │       
│                                     │       
│  ┌─────────────┐  ┌──────────────┐  │       
│  │  Rule-Based │  │ ML Predictor │  │       
│  │  Pipeline   │  │  (Joblib)    │  │       
│  └─────────────┘  └──────────────┘  │       
│         │                │          │       
│         ▼                ▼          │       
│  ┌──────────────────────────────┐   │       
│  │  LanguageTool + SpellCheck   │   │       
│  └──────────────────────────────┘   │       
└─────────────────────────────────────┘       
       │       
       ▼       
  JSON Response → Error List, Score, Corrected Text       
       
🔧 Tech Stack       
Backend       
       
Python 3.8+ — Core language       
Flask — REST API & web server       
Scikit-learn — ML model training & inference       
LanguageTool — Linguistic grammar rule engine       
PySpellChecker — Orthographic error detection       
NLTK — Text tokenization & preprocessing       
NumPy / Pandas — Data processing & feature engineering       
Joblib — Model serialization       
       
Frontend       
       
HTML5 / CSS3 / JavaScript — Clean, responsive UI       
Fetch API — Async backend communication       
       
Deployment       
       
Hugging Face Spaces — Cloud hosting & live demo       
       
       
🚀 Quick Start       
1. Clone the repository       
bashgit clone https://github.com/anmol8329/grammar-checker-tool.git       
cd grammar-checker-tool       
2. Install dependencies       
bashpip install -r requirements.txt       
3. Download NLTK data       
bashpython -c "import nltk; nltk.download('punkt')"       
4. Train ML models       
bashpython train.py       
       
📥 Download datasets from Kaggle before training.       
       
5. Start the backend server       
bashpython app.py       
6. Open the frontend       
bashcd frontend/       
python -m http.server 8000       
# Visit http://localhost:8000       
       
📡 API Reference       
POST /api/check       
Request:       
json{       
  "text": "He go to school yesterday."       
}       
Response:       
json{       
  "success": true,       
  "errors": [       
    {       
      "text": "go",       
      "correction": "went",       
      "type": "Tense Error",       
      "severity": "high",       
      "start": 3,       
      "end": 5       
    }       
  ],       
  "corrected_text": "He went to school yesterday.",       
  "score": 85,       
  "word_count": 5,       
  "error_count": 1       
}       
GET /api/health       
Health check endpoint for uptime monitoring.       
       
🛠️ Error Detection Coverage       
       
✅ Spelling Errors & Typos       
✅ Tense Inconsistencies       
✅ Subject-Verb Agreement       
✅ Modal Verb Errors       
✅ Article Mistakes (a/an)              
✅ Preposition Errors       
✅ Punctuation & Capitalization       
✅ Irregular Verb Forms       
       
       
📁 Project Structure       
grammar-checker/       
│       
├── app.py                   # Flask backend server & API routes       
├── train.py                 # ML model training pipeline       
├── grammar_predictor.py     # ML inference module       
├── requirements.txt         # Python dependencies       
│       
├── models/                  # Serialized ML models (Joblib)       
│   └── best_model.joblib       
│       
└── frontend/                # Web interface       
    ├── index.html       
    ├── style.css       
    └── script.js       
       
📊 ML Pipeline       
       
Preprocessing — Tokenization, POS tagging, and feature extraction via NLTK              
Rule-Based Detection — Fast, deterministic pattern matching for common errors       
ML Classification — Scikit-learn models trained on labeled grammar datasets       
LanguageTool Integration — Deep linguistic grammar rule coverage       
Spell Checking — PySpellChecker for orthographic corrections       
Score Aggregation — Weighted scoring outputs a 0–100 quality score       
       
👤 Author       
Anmol Tripathi       
🌐 Live Project       
📜 TCS iON Remote Internship · Dec 2024 – Mar 2025       
       
<p align="center"><i>Built during TCS iON Remote Internship · Tata Consultancy Services</i></p>
