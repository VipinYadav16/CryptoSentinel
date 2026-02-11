# CryptoSentinel

## Introduction

**CryptoSentinel** is an AI-driven security platform designed to protect Web3 investors from market manipulation and fraudulent activities. It leverages **advanced algorithms** and **deep on-chain analysis** to detect suspicious trading patterns, pump & dump schemes, and other deceptive practices in **real-time**.

By providing timely alerts and detailed market insights, CryptoSentinel empowers users to make informed decisions and safeguard their digital assets.

---

## 📑 Table of Contents

1. [Features](#features)
2. [Technical Implementation](#technical-implementation)
3. [Project Structure](#project-structure)
4. [Requirements](#project-requirements)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Configuration](#configuration)
8. [Examples](#examples)
9. [Troubleshooting](#troubleshooting)
10. [Contributors](#contributors)
11. [License](#license)

---

## ✨ Features

* **AI-Powered Fraud Detection** – Detects pump & dump schemes, phishing attempts, wash trading, and malicious smart contracts.
* **Real-Time Wallet Monitoring** – Push and email alerts for suspicious wallet activity.
* **Sentiment Analysis Engine** – Analyzes social media discussions and correlates them with token price movements.
* **Historical Pattern Matching** – Compares new activities with past fraud cases.
* **Privacy-First & Secure** – Non-custodial design with end-to-end encryption.

---

## ⚙️ Technical Implementation

### Frontend

* **Frameworks**: React + TypeScript + Vite
* **UI**: shadcn-ui + Tailwind CSS (custom themes + animations)
* **Routing**: `react-router-dom`
* **State Management**: `@tanstack/react-query`, `AuthContext`, and `ThemeContext`
* **Custom Components**: AuthForm, FraudAlerts, SentimentWidget, StockChart, Navbar, Footer, etc.

### Backend

* **Framework**: Flask (Python) with `flask_cors`
* **Anomaly Detection**: IsolationForest (scikit-learn) + TensorFlow Autoencoder
* **Data Source**: CoinGecko API
* **AI Analysis**: Google Gemini API (financial analysis persona)
* **Visualization**: `matplotlib` (via `plot_generator.py`)

### General

* **Authentication**: Mock auth with `localStorage` + React Context
* **Build Tools**: Vite, PostCSS, Tailwind, ESLint
* **Lock Files**: `package-lock.json` (npm), `bun.lockb` (Bun)

---

## 📂 Project Structure

```plaintext
CryptoSentinel/  
├── public/                 # Static assets (logo, favicon, generated plots)  
│   ├── pred/               # Generated plot images  
│   ├── favicon.png  
│   ├── lg.png  
│   └── logo.png  
├── src/  
│   ├── App.tsx             # Main app component + routing  
│   ├── components/         # UI Components (auth, dashboard, layout, etc.)  
│   ├── contexts/           # Auth + Theme contexts  
│   ├── hooks/              # Custom hooks (theme, toast, mobile detection)  
│   ├── lib/                # Utility functions  
│   └── pages/              # Pages (Index, Dashboard, Login, etc.)  
├── app.py                  # Flask backend server  
├── Graph.py                # Alternate anomaly detection script  
├── plot_generator.py       # Matplotlib chart generation  
├── .env                    # Environment variables (API keys)  
├── package.json            # Frontend dependencies  
├── requirements.txt        # Backend dependencies (Flask, scikit-learn, TensorFlow, etc.)  
└── vite.config.ts          # Vite config  
```

---

## 📦 Project Requirements

### Frontend

* React, TypeScript, Vite
* shadcn-ui, Tailwind CSS
* react-router-dom, @tanstack/react-query

### Backend

* Flask, flask\_cors
* scikit-learn, TensorFlow
* requests, matplotlib
* CoinGecko API, Google Gemini API

---

## ⚡ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/CryptoSentinel.git
cd CryptoSentinel
```

### Backend Setup

```bash
python -m venv venv
source venv/bin/activate   # (Linux/Mac)
venv\Scripts\activate      # (Windows)

pip install -r requirements.txt
```

### Frontend Setup

```bash
npm install
```

---

##  Usage

Start backend server:

```bash
python app.py
```

Start frontend dev server:

```bash
npm run dev
```

Frontend will be available at `http://localhost:5173`
Backend API at `http://localhost:5000`

---

## 🔧 Configuration

Create a `.env` file in the project root:

```ini
GEMINI_API_KEY=your_google_gemini_api_key
COINGECKO_API_URL=https://api.coingecko.com/api/v3
```

---

## 📊 Examples

* Run anomaly detection & generate a chart:

```bash
python plot_generator.py
```

This saves a PNG with marked anomalies in `public/pred/`.

---

## 🛠 Troubleshooting

* **Frontend build issues** → Delete `node_modules` and reinstall with `npm install`.
* **Backend missing dependencies** → Check `requirements.txt` and reinstall.
* **CORS issues** → Ensure `flask_cors` is enabled in `app.py`.
* **Invalid Gemini API Key** → Verify `.env` file is set correctly.

---

## 👥 Contributors

* **Shubham Tandon** 
* **Vihag Chaturvedi**
* **Vipin Yadav** 
* **Yajat Gupta** 

---

## 📜 License

This project is licensed under the [MIT License](https://choosealicense.com/licenses/mit/).

---
