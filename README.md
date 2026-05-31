# Oculon

**Oculon** is an AI-powered traffic surveillance project that detects incidents in real time, displays them on a polished React dashboard, and integrates cloud services for alerting and storage.

---

## Overview

Oculon is built to show modern full-stack engineering skills in a complete end-to-end system. It combines a Python backend with AI/ML capabilities, cloud infrastructure, and a professional frontend dashboard so recruiters can quickly understand the product and how it works.

The system is designed to:

- monitor traffic camera video feeds
- detect collisions, unusual activity, and incidents
- send alerts through AWS messaging services
- present real-time incident status and analytics in a dashboard

This project is ideal for demonstrating experience in AI-powered monitoring, cloud deployment, and user-friendly interface design.

---

## Tech stack

- **Frontend:** React, Tailwind CSS, React Router, custom UI components
- **Backend:** Python, Flask, Flask-CORS
- **AI / Vision:** YOLO object detection, Google Gemini generative visual model, OpenCV, Pillow, NumPy
- **Cloud / Infrastructure:** AWS S3, AWS SNS, AWS DynamoDB, AWS CloudFormation
- **Deployment / Tools:** Bash scripts, environment configuration, Docker-friendly architecture, Git

---

## Key features

- **Traffic incident detection** using a YOLO object detection model
- **AI analysis** of video/image frames with Google Gemini
- **Real-time dashboard** showing incidents, analytics, and video details
- **Incident alerts** via AWS SNS and cloud notifications
- **Video and incident feed** for operational monitoring
- **Modern UI** built with Tailwind CSS and reusable React components
- **Cloud-ready architecture** with AWS infrastructure scripts and guidance

---

## Process on creating the project

1. **Ideation and scope definition**
   - Defined the product goal: a traffic safety monitoring system that blends AI detection with an operations dashboard.
   - Identified business-facing value: faster incident awareness, improved road safety, and demonstrable cloud integration.

2. **Backend architecture**
   - Built a Flask API to handle video processing, incident detection, and cloud integration.
   - Integrated AWS services for storage, messaging, and incident persistence.
   - Connected Google Gemini to analyze frames and add contextual incident details.

3. **AI model integration**
   - Added YOLO-based object detection for real-time scene understanding.
   - Added a fallback mode for demo use when OpenCV or YOLO is unavailable.
   - Used AI output to classify incident types, severity, and descriptive text.

4. **Frontend design and dashboard implementation**
   - Created a clean dashboard using React and Tailwind CSS.
   - Built interactive components for surveillance views, incident feeds, and detailed video review.
   - Designed incident notifications and analytics cards for recruiter-friendly product presentation.

5. **Infrastructure and deployment**
   - Included setup scripts to streamline local development.
   - Provided AWS deployment flow and environment configuration.
   - Prepared shell scripts for backend and frontend startup.

---

## What I learned

- How to build a **full-stack application** that connects frontend, backend, AI, and cloud services.
- How to integrate **computer vision** with **ML inference** models in a production-style pipeline.
- How to connect **Google Gemini** with image data for richer incident analysis.
- How to use **AWS services** for storage, notifications, and serverless-friendly infrastructure.
- How to design a **front-end dashboard** that communicates system health and incident status clearly.
- How to package development flow with **setup scripts** and environment configuration for easier onboarding.

---

## How it can be improved

- Add **real streaming camera integration** instead of mock or sample video feeds.
- Increase **incident accuracy** by training or fine-tuning models on a dedicated traffic dataset.
- Add **user authentication** and role-based access control for a production-ready dashboard.
- Add **more incident categories** including pedestrians, weather hazards, and road damage.
- Improve **error handling** and monitoring for AWS service failures.
- Add a **demo mode** and clearer fallback behavior for non-technical users.
- Build a **production deployment** with Docker Compose, ECS/EKS, or a managed web hosting environment.

---

## How to run the project

### Prerequisites

- Python 3.9 or newer
- Node.js 18+ and npm
- Git
- Bash-compatible shell on Windows (Git Bash, WSL, or similar)
- AWS account and Google Gemini API access if you want full cloud/AI integration

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd Oculon
```

### 2. Create the `.env` file

```bash
cp env.example .env
```

Open `.env` and add your credentials and configuration values:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION`
- `SNS_TOPIC_ARN`
- `S3_BUCKET_NAME`
- `GEMINI_API_KEY`
- `FRONTEND_URL`
- `BACKEND_URL`

### 3. Install dependencies and prepare the app

Run the setup script from the repository root:

```bash
./setup.sh
```

This script will:

- create and activate a Python virtual environment in `backend`
- install backend dependencies from `backend/requirements.txt`
- download the YOLO model
- install frontend packages in `frontend`
- create required local folders and set up `.env`

### 4. Start the backend

```bash
cd backend
source venv/bin/activate
python app.py
```

The backend will be available at `http://localhost:5000`.

### 5. Start the frontend

In a second terminal:

```bash
cd frontend
npm start
```

The frontend dashboard will be available at `http://localhost:3000`.

### 6. Optional: deploy AWS infrastructure

If you have AWS configured, use the deployment script:

```bash
./aws/scripts/deploy.sh
```

This will create AWS resources such as S3, DynamoDB, SNS, and supporting roles.
