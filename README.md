🤖 Telegram AI Automation using n8n

An AI-powered Telegram bot built using **n8n** that receives messages, processes them with **Google Gemini AI**, and replies automatically.


## 🚀 Features

* 📩 Receive Telegram messages
* 🧠 AI-generated responses (Google Gemini)
* 💬 Auto-reply system
* 🧠 Optional memory for context
* ⚡ Fully automated workflow

---

## 🏗️ Workflow Architecture

```
Telegram Trigger → AI Agent → Send Message (Telegram)
```

---

## 🧩 Components

### 1. Telegram Trigger

* Listens to incoming messages from users

### 2. AI Agent

* Processes input using Google Gemini
* Can use memory for context retention

### 3. Send Message Node

* Sends response back to Telegram user

---

## 🛠️ Prerequisites

Make sure you have:

* Node.js (v18+)
* n8n installed
* Telegram account
* Google Gemini API key

---

## ⚙️ Installation & Setup

### 1. Install n8n

```bash
npm install n8n -g
n8n start
```

Open in browser:

```
http://localhost:5678
```

---

### 2. Create Telegram Bot

1. Open Telegram
2. Search for **@BotFather**
3. Run:

```
/start
/newbot
```

4. Copy your **Bot Token**

---

### 3. Setup HTTPS (Fix Webhook Error)

Telegram requires HTTPS — localhost won't work directly.

#### ✅ Use ngrok

```bash
ngrok http 5678
```

Example output:

```
https://abcd1234.ngrok.io
```

---

### 4. Configure Telegram in n8n

* Paste your **Bot Token**
* Set Webhook URL:

```
https://your-ngrok-url/webhook
```

---

### 5. Setup Google Gemini API

1. Visit: [https://ai.google.dev](https://ai.google.dev)
2. Generate API key
3. Add credentials in n8n:

   * Service: Google Gemini
   * Paste API Key

---

### 6. Configure AI Agent Node

* Connect:

  * Chat Model → Google Gemini
  * Memory → Simple Memory (optional)

---

### 7. Connect Workflow Nodes

Ensure correct flow:

```
Telegram Trigger → AI Agent → Send Message
```

---

## ▶️ How to Use

1. Start n8n
2. Run ngrok
3. Activate workflow in n8n
4. Open your Telegram bot
5. Send a message

✅ You’ll receive an AI-generated reply instantly

---

## 📂 Use Cases

* AI Chatbot
* Customer Support Bot
* Personal Assistant
* FAQ Automation
* Learning Assistant

---

## ⚠️ Common Errors & Fixes

### ❌ Bad Request: HTTPS required

**Fix:**

* Use ngrok OR deploy n8n on a server with HTTPS

---

### ❌ Bot not responding

Check:

* Workflow is **active**
* ngrok is running
* Webhook URL is correct

---

### ❌ AI not responding

Check:

* Gemini API key is valid
* AI Agent node is properly configured

---

## 🧠 Future Improvements

* WhatsApp integration
* Database (MongoDB / Notion)
* Voice input support
* Multi-language support
* Cloud deployment (Render / Railway / VPS)

---

## 📦 Tech Stack

* n8n (Automation)
* Telegram Bot API
* Google Gemini AI
* ngrok (HTTPS tunneling)

---

## 🙌 Author

**Vishal Waghmare**
AI Builder | Business Analyst | Automation Enthusiast

---

## ⭐ Support

If you found this useful:

* Star ⭐ the repository
* Share it
* Build your own automation 🚀

