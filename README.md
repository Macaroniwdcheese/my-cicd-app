# 🚀 my-cicd-app

[![CI/CD Build](https://github.com/Macaroniwdcheese/my-cicd-app/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/Macaroniwdcheese/my-cicd-app/actions)
[![DockerHub](https://img.shields.io/badge/DockerHub-macaroniwdcheese%2Fmy--cicd--app-blue?logo=docker)](https://hub.docker.com/r/macaroniwdcheese/my-cicd-app)

This project demonstrates a simple, beginner-friendly **CI/CD pipeline** using **GitHub Actions** to automatically:

- 🧪 Run tests
- 🐳 Build a Docker image
- ☁️ Push it to DockerHub
- 🛠️ (Optional) Deploy it to any server or cloud

---

## 🧱 CI/CD Flow Overview

### 1. ✅ Build & Run the App Locally

Flask app running locally (development preview):

![Local App Running](https://github.com/user-attachments/assets/3e0d1008-fba2-4a58-9921-0e32bf32a6da)

---

### 2. 🧪 Run Automated Tests

- Tests run automatically via `pytest`
- Ensures the app doesn't crash and returns expected results

✅ Protects your main branch from broken code

---

### 3. 🐳 Build a Docker Image

- Your app is packaged with its dependencies using Docker
- Ensures consistency across all environments

---

### 4. ☁️ Push to DockerHub

The Docker image is uploaded to:

🔗 [`macaroniwdcheese/my-cicd-app`](https://hub.docker.com/r/macaroniwdcheese/my-cicd-app)

---

### 5. 🚀 Trigger on Main Branch Commits

Every push to the `main` branch runs the pipeline automatically via GitHub Actions.

---

### 6. 🌍 (Optional) Deploy Anywhere

You can deploy the image from DockerHub to:

- ✅ Azure, AWS, Google Cloud
- ✅ A Linux server with Docker
- ✅ Raspberry Pi

---

### 7. 🔔 Add Notifications (Optional)

Get build/deploy results via:

- 📩 Email
- 💬 Slack
- 🛎️ Discord

---

## 💡 Stack Used

| Tool        | Purpose                        |
|-------------|---------------------------------|
| Python 3.11 | Application runtime             |
| Flask       | Web framework                   |
| Pytest      | Test runner                     |
| Docker      | Containerization                |
| GitHub Actions | CI/CD automation             |

---

## 🧰 Run Locally

```bash
# Install dependencies
pip install -r requirements.txt

# Run the app
python3 app/main.py


Then open http://localhost:5000 in your browser.
