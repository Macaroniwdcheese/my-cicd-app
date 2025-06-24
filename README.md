# 🚀 my-cicd-app

This project demonstrates a **simple CI/CD pipeline** using **GitHub Actions** to automatically build, test, and deploy a Python (Flask) application inside a Docker container.

---

## 📦 What This Pipeline Does

### 1. ✅ Build & Run the App Locally

You can run the app locally with Flask. Example:

![Local App Running](https://github.com/user-attachments/assets/3e0d1008-fba2-4a58-9921-0e32bf32a6da)

---

### 2. 🧪 Run Automated Tests

Before deployment, the pipeline:

- Runs Python unit tests (with `pytest`)
- Ensures the app doesn't crash and returns expected results

✅ Helps catch bugs before pushing broken code into production.

---

### 3. 🐳 Build a Docker Image

The pipeline packages your app into a Docker image containing:

- Your application code
- Python runtime
- Flask and required libraries

✅ This guarantees it runs identically on any machine or cloud.

---

### 4. ☁️ Push to DockerHub

Your Docker image is pushed to your DockerHub account:

🔗 `macaroniwdcheese/my-cicd-app:latest`

---

### 5. 🚀 Trigger on Main Branch Commits

The pipeline runs automatically **on every push to the `main` branch** — no manual work needed.

---

### 6. 🌍 (Optional) Deploy to Any Environment

Once your image is in DockerHub, you can deploy it to:

- **Azure**, **AWS**, or **Google Cloud**
- **Raspberry Pi**
- Any server with Docker installed

---

### 7. 🔔 Notifications (Optional)

You can also add email or Slack notifications to alert you of:

- ✅ Successful builds
- ❌ Failed tests or builds

---

## 💡 Technologies Used

- GitHub Actions
- Python 3.11
- Flask
- Pytest
- Docker & DockerHub

---

## 🧰 How to Run Locally

```bash
# Install dependencies
pip install -r requirements.txt

# Run the app
python3 app/main.py
