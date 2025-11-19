# 🌿 **Solace AI**

### Emotion-Aware Conversational Companion (React + FastAPI + Docker)

Solace AI is a full-stack emotional support chatbot built with a **React + TailwindCSS** frontend and a **FastAPI** backend powered by the OpenAI API.
It provides empathetic conversation, emotion detection, and crisis-aware responses.

The project includes a complete Dockerized workflow for simple local development and deployment.

---

## 🚀 Features

* Emotion classification using LLM inference
* Empathetic conversational responses
* Crisis phrase detection
* FastAPI backend with REST endpoint (`/chat`)
* Modern React UI styled with TailwindCSS
* Fully containerized with Docker
* Clean separation of frontend and backend
* Production-ready build setup

---

## 🏗️ Tech Stack

### **Frontend**

* React
* TailwindCSS
* Vite
* JavaScript/TypeScript

### **Backend**

* FastAPI
* OpenAI Python SDK
* Uvicorn
* Python 3.10+

### **Deployment / Infra**

* Docker
* Docker Compose

---

## 📦 Repository Structure

```
Solace-AI/
│
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── Dockerfile
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   ├── Dockerfile
│
└── docker-compose.yml
```

---

## ⚙️ Running Locally (Docker)

You must set your OpenAI API key before running:

### **Linux / macOS**

```bash
export OPENAI_API_KEY=sk-xxxx
```

### **Windows PowerShell**

```powershell
$env:OPENAI_API_KEY="sk-xxxx"
```

### **Start both frontend + backend**

```bash
docker compose up --build
```

### **Access the app**

* Frontend → [http://localhost:3000](http://localhost:3000)
* Backend API → [http://localhost:8000](http://localhost:8000)
* API Docs → [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 📡 Backend API

### **POST /chat**

Request:

```json
{
  "message": "I feel overwhelmed today.",
  "history": []
}
```

Response:

```json
{
  "emotion": "stress",
  "reply": "I'm really sorry you're feeling overwhelmed. I'm here with you."
}
```

---

## 🔐 Environment Variables

| Variable         | Description                    |
| ---------------- | ------------------------------ |
| `OPENAI_API_KEY` | Your OpenAI API key (required) |

---

## 🧪 Development (Non-Docker)

### Backend:

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend:

```bash
cd frontend
npm install
npm run dev
```

---

## 📦 Production Build (Docker)

To build production images:

```bash
docker compose build
```

To run them:

```bash
docker compose up
```

---

## 📄 License

MIT License.
Feel free to use, modify, and extend Solace AI.

---
