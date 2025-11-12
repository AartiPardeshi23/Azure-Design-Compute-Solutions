
---

## 🧱 **lab4-app-service-plan-deploy.md**
```markdown
# AZ-305 Module 08 - Lab 4: Create an App Service Plan and Deploy Custom Web App

## 🎯 Objective
Deploy a custom Python app to Azure App Service using Zip Deploy.

---

## 🪜 Steps

### Step 1: Create Resource Group
- Name: `rg-az305-webapp`
- Region: East US

---

### Step 2: Create App Service Plan
1. Search **App Service Plans** → **+ Create**
2. Resource group: `rg-az305-webapp`
3. Name: `asp-az305-web`
4. OS: Linux
5. Pricing: B1 (Basic)
6. Review + Create → Create

---

### Step 3: Create Web App
1. Search **App Services** → **+ Create**
2. Resource group: `rg-az305-webapp`
3. Name: `app-az305-web`
4. Publish: Code
5. Runtime stack: Python 3.10
6. OS: Linux
7. App Service Plan: `asp-az305-web`
8. Review + Create → Create

---

### Step 4: Create Sample App Files
Create 3 files locally:

**app.py**
```python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def home():
    return "<h1>Hello from Azure App Service! 🎉</h1>"


### Step 5: Deploy Using Zip Deploy

### 

1.  Go to your Web App → **Deployment Center**
    
2.  Source: **Zip Deploy**
    
3.  Upload `hello.zip`
    
4.  Wait for deployment to complete
    
5.  Restart the App
    

* * *

### Step 6: Test the App

### 

*   Copy your URL (e.g., `https://app-az305-web.azurewebsites.net`)
    
*   Open in browser →  
    ✅ Shows: **“Hello from Azure App Service! 🎉”**