# 🧪 ADMET Prediction Web App

A full-stack web application for predicting **ADMET properties** (Absorption, Distribution, Metabolism, Excretion and Toxicity) of molecules using **SMILES input**.  
This project integrates a **React (frontend)** with a **Flask (backend)** and provides an interactive, mobile-friendly interface for visualizing molecular properties and market suitability.

---

## ✨ Features

- 🌐 **Frontend**:  
  - Built with **React + Tailwind CSS**  
  - Mobile-friendly, responsive UI  
  - Molecule drawing and SMILES input  
  - Beautiful animated dark/light theme toggle 🌙☀️  
  - Interactive prediction results with tables, plots and conclusion messages  

- ⚙️ **Backend**:  
  - **Flask API** serving prediction requests  
  - Integration with open-source ADMET models  
  - SMILES → Molecular rendering using **RDKit**  
  - JSON-based communication with frontend  

- 📊 **Results View**:  
  - Per-property ADMET predictions (Absorption, Distribution, Metabolism, Excretion, Toxicity)  
  - Overall category status (Good / Moderate / Poor)  
  - Professional market release suitability message with color-coded conclusion  

---

## 📂 Project Structure
admet-prediction-app/
├── admet_data/                 # ADMET datasets
├── backend/                    # Flask backend + saved models
│   ├── app.py
│   ├── utils/
│   └── requirements.txt
├── frontend/                   # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── assets/
│   │   ├── App.jsx
│   │   └── index.js
│   └── package.json
├── model_predictions/          # Predicted outputs
├── model_training/             # Model training scripts/notebooks
├── paths.py                    # Centralized paths
├── .gitignore
└── README.md

---

## ⚙️ Installation

### 1. Clone the repository

git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

### 2. Backend Setup

Create a virtual environment and install dependencies:
cd backend
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt

Run the backend:
python app.py

By default, it runs on http://127.0.0.1:5000

### 3. Frontend Setup

cd frontend
npm install
npm run dev

Frontend runs on http://localhost:5173

---

## 📡 API Endpoints

POST /predict → Takes SMILES string, returns ADMET prediction JSON.

Example:

{
  "smiles": "CCO",
  "Absorption": [...],
  "Distribution": [...],
  "Metabolism": [...],
  "Excretion": [...],
  "Toxicity": [...]
}

---

## 📝 License

MIT License © 2025 [Sheik Arshad Ibrahim]