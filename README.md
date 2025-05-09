# 🏨💬 AI Room Booking Chatbot — IBM Watson Assistant + Cloud Functions

![IBM Watson](https://img.shields.io/badge/Powered%20by-IBM%20Watson-blue?style=for-the-badge&logo=ibm)
![Cloud Functions](https://img.shields.io/badge/Cloud%20Functions-Enabled-brightgreen?style=for-the-badge&logo=ibmcloud)
![Language](https://img.shields.io/badge/Python-3.7-blue.svg?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)

Welcome to the **AI Room Booking Chatbot** project! This project uses **IBM Watson Assistant** for AI conversation and **IBM Cloud Functions** to send booking confirmation emails via Gmail.

---

## 🚀 Features

- 💬 Natural language chatbot using **Watson Assistant**
- 📧 Automatic email notifications via **IBM Cloud Functions**
- 🔐 Gmail App Password integration for secure email sending
- 🌐 Fully serverless architecture (No backend required!)

---

## 📦 Tech Stack

| Feature           | Tech Used                       |
|------------------|----------------------------------|
| 💡 AI Chatbot     | IBM Watson Assistant             |
| ⚙️ Serverless Logic | IBM Cloud Functions (Python 3.7) |
| 📧 Email Service   | Gmail SMTP + App Password        |
| 🌍 Webhook Linkage | Watson Webhooks + Web Actions    |

---

## 📝 Setup Guide

### 🔹 Step 1: IBM Cloud Account

1. 🌐 Create an account at 👉 [IBM Cloud Registration](https://cloud.ibm.com/registration)
2. 🔐 Already have one? [Login here](https://cloud.ibm.com/login)

---

### 🔹 Step 2: Create Watson Assistant

1. 🚀 Go to [IBM Watson Assistant Catalog](https://cloud.ibm.com/catalog/services/watson-assistant)
2. 🧠 Name your service and click **Create**
3. 🔧 Click **Launch Watson Assistant**
4. ➕ Click on **Create assistant**, then:
   - Give it a name and (optional) description
   - Click **Add an action or dialog skill**
   - Choose **Upload skill**
   - Upload `skill-Room-Booking.json`

> ✅ You now have a functional chatbot UI!

---

### 🔹 Step 3: Configure IBM Cloud Function

1. 🧭 Go to [IBM Cloud Functions](https://cloud.ibm.com/functions/actions)
2. ➕ Click **Create → Action**
   - Name your action
   - Leave package as **default**
   - Select **Python 3.7** runtime
   - Click **Create**

3. ✍ Paste the contents of `IBM_Cloud_Function.py` into the editor

---

### 🔹 Step 4: Gmail App Password

1. 🔐 Visit [Google Account Security](https://myaccount.google.com/security)
2. Enable **2-Step Verification**
3. Under **App Passwords**:
   - App: `Mail`
   - Device: `Other` → Name it something like `IBM Cloud Function`
   - Copy the generated password

4. 🔧 Paste this app password in line 10 of your cloud function code

---

### 🔹 Step 5: Connect Watson Assistant to Cloud Function

1. 🔗 In IBM Cloud Functions:
   - Click **Endpoints**
   - Enable as **Web Action**
   - Copy the public URL (append `.json` at the end)

2. 🔁 In Watson Assistant:
   - Go to `Options → Webhooks`
   - Paste your URL here

> 🥳 Done! Your chatbot can now send booking emails!

---

## 📸 Demo Screenshot (Optional)

> _(Add a screenshot or GIF here if you want visual proof of working bot UI!)_

---

## 🧪 Sample Booking Flow

```
User: I want to book a meeting room.
Bot: Sure, please provide the date and time.
User: Tomorrow at 2 PM.
Bot: Booking confirmed! A confirmation email has been sent.
```

---

## ✅ Final Checklist

- [x] IBM Watson Assistant created
- [x] Custom skill uploaded
- [x] IBM Cloud Function deployed
- [x] Gmail App Password configured
- [x] Webhook linked in Watson Assistant

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## ❤️ Credits

- IBM Watson Assistant
- IBM Cloud Functions
- Google SMTP for email
