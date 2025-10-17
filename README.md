# 🧪 ADMET Prediction Web App

<div align="center">
  <!-- Badges -->
  <p>
    <a href="https://admet-x.vercel.app/"><img src="https://img.shields.io/badge/Live-Webpage-green" alt="LIVE Website"></a>
    <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
    <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.12-blue.svg" alt="Python"></a>
    <a href="https://reactjs.org/"><img src="https://img.shields.io/badge/React-18.2.0-blue.svg" alt="React"></a>
    <a href="https://vitejs.dev/"><img src="https://img.shields.io/badge/Vite-React-orange.svg" alt="Vite + React"></a>
    <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker-Container-blue.svg" alt="Docker"></a>
    <a href="https://fly.io/"><img src="https://img.shields.io/badge/Deployment-Fly.io-purple.svg" alt="Fly.io"></a>
    <a href="https://vercel.com/"><img src="https://img.shields.io/badge/Deployment-Vercel-purple.svg" alt="Vercel"></a>
    <a href="https://www.rdkit.org/"><img src="https://img.shields.io/badge/RDKit-Chemistry-green.svg" alt="RDKit"></a>
    <a href="https://flask.palletsprojects.com/"><img src="https://img.shields.io/badge/Flask-Backend-orange.svg" alt="Flask"></a>
    <a href="https://framer.com/motion/"><img src="https://img.shields.io/badge/FramerMotion-Animation-red.svg" alt="Framer Motion"></a>
    <a href="https://lottiefiles.com/"><img src="https://img.shields.io/badge/Lottie-Animations-blue.svg" alt="Lottie"></a>
  </p>
</div>

A full-stack web application for predicting **ADMET properties** (Absorption, Distribution, Metabolism, Excretion and Toxicity) of molecules using **SMILES input**.

This project integrates a **React frontend** with a **Flask backend** and provides an interactive, mobile-friendly interface for visualizing molecular properties and market suitability.

---

## ✨ Features

### 🌐 Frontend

* Built with **React + Tailwind CSS**
* Mobile-friendly, responsive UI
* Molecule drawing and SMILES input
* Beautiful animated dark/light theme toggle 🌙☀️
* Interactive prediction results with tables, plots and conclusion messages

### ⚙️ Backend

* **Flask API** serving prediction requests
* Integration with open-source ADMET models
* SMILES → Molecular rendering using **RDKit**
* JSON-based communication with frontend

### 📊 Results View

* Per-property ADMET predictions: Absorption, Distribution, Metabolism, Excretion, Toxicity
* Overall category status: **Good / Moderate / Poor**
* Professional market release suitability message with color-coded conclusion

---

## 📂 Project Structure

```
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
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

> By default, the backend runs on: [http://127.0.0.1:5000](http://127.0.0.1:5000)

### 3. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

> Frontend runs on: [http://localhost:5173](http://localhost:5173)

---

## 🌐 Frontend(Vercel) Deployment

Follow these steps to deploy your **ADMET Prediction Frontend** using **Vercel**.

### 1. Push Frontend to GitHub

Make sure your frontend folder contains the following files and directories:

```
frontend/
├── .env.local
├── .env.production
├── vite.config.js
├── package.json
└── src/
```

### 2. Set Environment Variables

In your **`.env.production`** file, add the backend API URL (your Fly.io backend):

```bash
VITE_BACKEND_URL=https://admet-backend.fly.dev
```

### 3. Deploy to Vercel

Go to https://vercel.com

Click “New Project” → “Import Git Repository”

Choose your frontend repository

In Project Settings, set the following values:

| Setting                  | Value                                                 |
| ------------------------ | ----------------------------------------------------- |
| **Framework Preset**     | `Vite`                                                |
| **Build Command**        | `npm run build`                                       |
| **Output Directory**     | `dist`                                                |
| **Install Command**      | `npm install`                                         |
| **Environment Variable** | `VITE_BACKEND_URL=https://admet-backend.fly.dev` |

### Deployment Success

Once deployment completes, you’ll receive a live URL such as:

```bash
https://admet-x.vercel.app
```

---

## 📡 API Endpoints

**POST** `/predict` → Takes a SMILES string and returns ADMET prediction JSON.

Example request:

```json
{
  "smiles": "CCO",
  "Absorption": [...],
  "Distribution": [...],
  "Metabolism": [...],
  "Excretion": [...],
  "Toxicity": [...]
}
```

---

### 👥 Contributors
| Name                 | GitHub                                     | LinkedIn                                               |
| ---------------------| ------------------------------------------ | ------------------------------------------------------ |
| Rohith Reddy G K     | [GitHub](https://github.com/RohithReddyGK)  | [LinkedIn](https://www.linkedin.com/in/rohithreddygk/)  |
| Sheik Arshad Ibrahim | [GitHub](https://github.com/arshadibrahim882) | [LinkedIn](https://www.linkedin.com/in/sheik-arshad-ibrahim/) |
| Sayed Jahangir Ali   | [GitHub](https://github.com/Jahangir-ali-74)      |  -  |
| Thirumurugan M       | [GitHub](https://github.com/thirumuruganmeganath-ops)      |  -     |

---

## 📝 License

This project is licensed under the [MIT License](./LICENSE) © 2025 (ADMET-X Team)  
[**Sheik Arshad Ibrahim**](https://github.com/arshadibrahim882) 
