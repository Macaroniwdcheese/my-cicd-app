# my-cicd-app
Lets build a simple CI/CD pipeline using GitHub Actions to:

    Build your app and run locally
    
    Run tests

    Build and push a Docker image

    Trigger on main branch commits

    Notify you on success/failure (via email or Slack)

🧱 Step 1: Create Your Project Folder and Files
1. 📁 Create a new directory for your app
   mkdir my-cicd-app
    cd my-cicd-app

2. 🐍 Create the app code    
Create app/main.py:
mkdir app
nano app/main.py

Paste this code:
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
return "Hello, CI/CD!"

Press Ctrl+O, then Enter to save, and Ctrl+X to exit.

3. 📦 Create requirements.txt

nano requirements.txt
Add this:

flask

4. 🧪 Add a basic test
Create tests/test_app.py

mkdir tests
nano tests/test_app.py

Paste this code:

from app.main import app

def test_home():
client = app.test_client()
response = client.get('/')
assert response.data == b"Hello, CI/CD!"

5. 🐳 Create a Dockerfile

nano Dockerfile

Paste:

FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["python", "app/main.py"]

✅ Confirm structure

You should now have this:

my-cicd-app/
├── app/
│   └── main.py
├── tests/
│   └── test_app.py
├── Dockerfile
└── requirements.txt

6. 🚀 Test Locally (optional)

If you want to try it locally:

pip install -r requirements.txt
python app/main.py

Then open a browser at http://localhost:5000
