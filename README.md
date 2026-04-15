# 🚀 STGNN Traffic Forecasting System (DevOps + Azure Deployment)

## 📌 Project Overview

This project implements a **Spatio-Temporal Graph Neural Network (STGNN)** for traffic prediction and forecasting, deployed using a full **DevOps pipeline**.

The system includes:

* 🧠 Deep Learning model for traffic prediction
* ⚙️ FastAPI backend for serving predictions
* 🌐 Frontend UI (Dockerized)
* 🐳 Containerized services using Docker
* 🔁 CI/CD pipeline using Jenkins
* ☁️ Cloud deployment on Microsoft Azure

---

## 🏗️ Architecture

```
Frontend (NGINX on Azure)
        ↓
FastAPI Backend (Azure App Service)
        ↓
STGNN Model (PyTorch)
```

---

## 🧰 Tech Stack

### 🔹 Machine Learning

* Python
* PyTorch
* STGNN (Spatio-Temporal Graph Neural Network)

### 🔹 Backend

* FastAPI
* Uvicorn

### 🔹 Frontend

* React (served via NGINX container)

### 🔹 DevOps

* Docker
* Docker Compose
* Jenkins (CI/CD)

### 🔹 Cloud

* Microsoft Azure App Service
* Azure Container Registry (ACR)

---

## 📁 Project Structure

```
APD Project/
│
├── api/                  # FastAPI backend
│   ├── main.py
│   └── __init__.py
│
├── data/                 # Dataset (METR-LA, PEMS-BAY)
├── checkpoints/          # Trained model checkpoints
│
├── docker/
│   └── Dockerfile.api    # Backend Dockerfile
│
├── docker-compose.yml    # Multi-container setup
├── requirements.txt      # Python dependencies
└── stgnn-docker.tar      # Prebuilt Docker image
```

---

## ⚙️ How to Run Locally

### 1️⃣ Start Docker

Make sure Docker Desktop is running.

---

### 2️⃣ Run using Docker Compose

```bash
docker compose up --build
```

---

### 3️⃣ Access services

* Frontend → http://localhost:3000
* Backend → http://localhost:8000

---

## ☁️ Azure Deployment

### 🔹 Steps followed:

1. Created **Azure Container Registry (ACR)**
2. Built Docker images for:

   * Backend (FastAPI)
   * Frontend (NGINX)
3. Pushed images to ACR
4. Deployed using **Azure App Service (Linux Container)**
5. Configured environment variables (e.g., `WEBSITES_PORT`)

---

### 🔹 Live Application

👉 Frontend:
https://stgnn-app-123-ajavbbfheuc6g0cz.centralindia-01.azurewebsites.net

---

## 🔁 CI/CD Pipeline

* Integrated with **Jenkins**
* Pipeline steps:

  * Pull code from GitHub
  * Build Docker images
  * Push to ACR
  * Deploy to Azure

---

## 📊 Model Details

* Model: **STGNN (Spatio-Temporal Graph Neural Network)**
* Dataset:

  * METR-LA
  * PEMS-BAY
* Input: Traffic sensor data
* Output: Future traffic predictions

---

## ⚠️ Notes

* Frontend is served using **NGINX (port 80)** in production
* Backend runs on **port 8000**
* Environment variables are used to configure API endpoints

---

## 👨‍💻 Author

**Jaden Castelino**

---

## ⭐ Future Improvements

* Kubernetes deployment (scaling)
* Better UI/UX
* Real-time streaming data
* Monitoring with Azure Insights

---

## 📌 Conclusion

This project demonstrates a complete **end-to-end ML + DevOps pipeline**, including:

* Model training
* API development
* Containerization
* CI/CD
* Cloud deployment

---
