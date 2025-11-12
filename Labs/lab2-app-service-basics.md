# AZ-305 Module 08 - Lab 2: Azure App Services Basics

## 🎯 Objective
Learn to deploy a simple web app using Azure App Service (without managing servers).

---

## 🪜 Steps

### Step 1: Create a Resource Group
1. Search **Resource Groups** → **+ Create**
2. Name: `rg-az305-appservice`
3. Region: East US

---

### Step 2: Create App Service Plan
1. Search **App Service Plans** → **+ Create**
2. Resource group: `rg-az305-appservice`
3. Name: `asp-az305`
4. OS: Linux
5. Region: East US
6. Pricing: **B1 (Basic)**
7. Review + Create → Create

---

### Step 3: Create Web App
1. Search **App Services** → **+ Create**
2. Resource group: `rg-az305-appservice`
3. Name: `app-az305-demo`
4. Publish: **Code**
5. Runtime stack: **Python 3.10**
6. OS: **Linux**
7. App Service Plan: `asp-az305`
8. Review + Create → Create

---

### Step 4: Verify the App
- Go to **App Services → app-az305-demo**
- Click the **URL** (e.g., `https://app-az305-demo.azurewebsites.net`)
- You should see: **“Your web app is running”**

✅ You’ve successfully created a live web app on Azure.
