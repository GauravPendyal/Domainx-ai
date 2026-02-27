# DomainX AI

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B3C5D,100:1F6AE1&height=180&section=header&text=DomainX%20AI&fontSize=56&fontAlignY=35&animation=fadeIn&fontColor=ffffff"/>

### AI-Powered Job Discovery & Resume Intelligence Platform

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&duration=2800&pause=1000&color=1F6AE1&center=true&vCenter=true&width=680&lines=AI-Powered+Job+Discovery+Platform;ATS+Resume+Analysis+Engine;Python+ML+Semantic+Matching;Service-Oriented+Backend" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white"/>
  <img src="https://img.shields.io/badge/sentence--transformers-FF6F00?style=for-the-badge&logo=huggingface&logoColor=white"/>
  <img src="https://img.shields.io/badge/OAuth-4285F4?style=for-the-badge&logo=google&logoColor=white"/>
</p>

</div>

---

## 💡 What is DomainX AI?

**DomainX AI** is a full-stack, AI-powered career intelligence platform that combines:

- **ATS Resume Analysis** — Score your resume against hiring algorithms
- **Python ML Microservice** — Semantic job matching via `sentence-transformers` (MiniLM)
- **Real-Time Job Search** — Live jobs via Jooble API
- **AI Skill Assessment** — MCQ tests across 6 domains, powered by AI
- **Career Discovery** — Discover your best-fit domain using AI scoring

---

## 🏗️ Architecture

```
Frontend (HTML/CSS/JS)
       ↓
Auth Server     (Node.js · port 8000) — Google OAuth + JWT
Main API Server (Node.js · port 5000) — Jobs, Dashboard, Saved Jobs  
Resume Server   (Node.js · port 5001) — ATS Analysis + Resume History
       ↓
ML Microservice (Python FastAPI · port 8001) — Semantic Job Matching
```

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 📄 ATS Resume Scoring | Structured resume analysis with skills, strengths, weaknesses |
| 🤖 ML Job Matching | `paraphrase-MiniLM-L3-v2` semantic similarity against 20 curated jobs |
| 🌍 Live Job Feed | Real-time jobs from Jooble API |
| 🔐 Auth System | Google OAuth 2.0 + JWT |
| 🎯 Skill Tests | AI-generated MCQ assessments per domain |
| 📊 Performance Dashboard | Skill breakdown, company recommendations, global rank |

---

## 🧰 Tech Stack

| Layer | Technologies |
|-------|-------------|
| Frontend | HTML5, CSS3, Vanilla JS |
| Auth Server | Node.js, Express, Passport, JWT |
| API Server | Node.js, Express, MongoDB |
| Resume Server | Node.js, Express, Multer, pdf-parse |
| ML Service | Python, FastAPI, sentence-transformers, scikit-learn |
| Database | MongoDB |
| Job API | Jooble Search API |

---

## ⚙️ Installation

### 1. Clone

```bash
git clone https://github.com/GauravPendyal/domainx-ai.git
cd domainx-ai
```

### 2. Install Node dependencies

```bash
npm install
npm install --prefix auth-server
npm install --prefix resume-server
npm install --prefix server
```

### 3. Install Python ML dependencies

```bash
cd ml-service
pip install -r requirements.txt
```

### 4. Configure environment

```bash
cp .env.example .env
# Fill in your credentials
```

### 5. Run all services

```bash
# Terminal 1 — All Node servers
npm run dev

# Terminal 2 — Python ML microservice
cd ml-service
python -m uvicorn ml_service:app --reload --port 8001
```

---

## 🔐 Environment Variables

See `.env.example` for all required variables. Never commit `.env`.

---

## 📂 Project Structure

```
domainx-ai/
├── client/              # Frontend HTML/CSS/JS
├── server/              # Main API (jobs, dashboard)
├── auth-server/         # Google OAuth + JWT
├── resume-server/       # ATS resume analysis
├── ml-service/          # Python FastAPI ML microservice
│   ├── ml_service.py
│   └── requirements.txt
├── package.json
├── .env.example
└── README.md
```

---


---

⭐ **Star this repo if it helps you land your dream job!**
Made with ❤️ for job seekers worldwide
