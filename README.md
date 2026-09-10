# 🤖 MethzBot — AI-Powered Telegram Chatbot

<p align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square\&logo=openai\&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=flat-square\&logo=telegram\&logoColor=white)
![Aiogram](https://img.shields.io/badge/Aiogram-2.25.2-2CA5E0?style=flat-square\&logo=telegram\&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-000000?style=flat-square\&logo=railway\&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square\&logo=github\&logoColor=white)

![python-dotenv](https://img.shields.io/badge/python--dotenv-3776AB?style=flat-square\&logo=python\&logoColor=white)
![AsyncIO](https://img.shields.io/badge/AsyncIO-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)

</p>

<p align="center">
  <b>AI-powered conversational chatbot built with Python, Aiogram, Telegram, and OpenAI.</b>
</p>

---

## 📌 Overview

**MethzBot** is an AI-powered Telegram chatbot developed using **Python**, **Aiogram**, and the **OpenAI API**.

The chatbot allows users to communicate with an AI assistant directly through Telegram. It supports conversational interactions, useful bot commands, environment-variable based API-key management, and cloud deployment using Railway.

This project demonstrates how to integrate a modern AI API with a real-world messaging platform.

---

## ✨ Features

* 🤖 AI-powered conversational responses
* 💬 Telegram-based chat interface
* 🧠 Conversation context handling
* 🧹 `/clear` command to reset conversation context
* 🚀 `/start` command for bot initialization
* ❓ `/help` command for available commands
* 🔐 Secure API-key management using `.env`
* ⚡ Asynchronous Telegram bot architecture
* ☁️ Railway deployment support
* 🐍 Built entirely with Python

---

## 🏗️ Architecture

```text
                    ┌──────────────────────┐
                    │       Telegram       │
                    │        User          │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │      MethzBot        │
                    │      Aiogram         │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │     OpenAI API       │
                    │   AI Conversation    │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   AI Generated       │
                    │      Response        │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │      Telegram        │
                    │       User           │
                    └──────────────────────┘
```

---

## 🔄 How It Works

```text
User sends message
        ↓
Telegram receives message
        ↓
Aiogram processes message
        ↓
MethzBot sends request to OpenAI
        ↓
OpenAI generates AI response
        ↓
Response returned to MethzBot
        ↓
Bot sends response to user
```

---

## 🛠️ Technologies

| Technology    | Purpose                         |
| ------------- | ------------------------------- |
| Python        | Core programming language       |
| Aiogram       | Telegram Bot framework          |
| OpenAI API    | AI-generated responses          |
| Telegram      | User interface                  |
| AsyncIO       | Asynchronous execution          |
| python-dotenv | Environment variable management |
| Git           | Version control                 |
| GitHub        | Source code hosting             |
| Railway       | Cloud deployment                |

---

## 📂 Project Structure

```text
TELEGRAM-CHATBOT/
│
├── main.py
├── requirements.txt
├── .env
├── .gitignore
├── README.md
│
└── research/
    └── mybot/
```

> `research/mybot/` is a local Python virtual environment and should **not** be uploaded to GitHub.

---

## 💻 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

```bash
cd TELEGRAM-CHATBOT
```

### 2. Create a Virtual Environment

```bash
python -m venv research/mybot
```

### 3. Activate the Environment

**Windows:**

```bash
research\mybot\Scripts\activate
```

**Linux / macOS:**

```bash
source research/mybot/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
OPENAI_API_KEY=your_openai_api_key
```

### ⚠️ Security

Never upload your `.env` file to GitHub.

Your `.gitignore` should contain:

```gitignore
.env
mybot/
research/mybot/
__pycache__/
*.pyc
.vscode/
```

---

## ▶️ Run Locally

After activating the virtual environment:

```bash
python main.py
```

If everything is configured correctly, MethzBot will start listening for Telegram messages.

---

## 🤖 Bot Commands

| Command  | Description                |
| -------- | -------------------------- |
| `/start` | Start the chatbot          |
| `/help`  | Display available commands |
| `/clear` | Clear conversation context |

### `/start`

Example:

```text
Hi!

I am MethzBot!
Created by MethzAI.

How can I assist you?
```

### `/clear`

Example:

```text
I've cleared the past conversation and context.
```

---

## 💬 Example Interaction

```text
User:
What is Artificial Intelligence?

MethzBot:
Artificial Intelligence is a field of computer science
that focuses on creating systems capable of performing
tasks that normally require human intelligence...
```

---

## 🧠 Conversation Context

MethzBot can maintain conversation context while the application is running.

This allows the AI to understand previous messages and provide more relevant responses.

For example:

```text
User:
What is Python?

Bot:
Python is a high-level programming language...

User:
What are its advantages?

Bot:
Some major advantages of Python are...
```

The `/clear` command can be used to reset the conversation context.

---

## 📦 Requirements

The project uses the following main dependencies:

```text
aiogram==2.25.2
openai==0.28.0
python-dotenv==0.21.1
```

Install them with:

```bash
pip install -r requirements.txt
```

---

## ☁️ Railway Deployment

MethzBot can be deployed to **Railway** for cloud hosting.

### Step 1 — Push Project to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

### Step 2 — Create Railway Project

Create a new Railway project and connect your GitHub repository.

### Step 3 — Add Environment Variables

Add:

```text
TELEGRAM_BOT_TOKEN
OPENAI_API_KEY
```

with their corresponding values.

### Step 4 — Start Command

Use:

```bash
python main.py
```

Railway will then install the dependencies and start the bot.

---

## 🚀 Deployment Architecture

```text
              GitHub Repository
                     │
                     ▼
                ┌─────────┐
                │ Railway │
                └────┬────┘
                     │
                     ▼
                ┌─────────┐
                │ MethzBot│
                └────┬────┘
                     │
              ┌──────┴──────┐
              ▼             ▼
        Telegram API     OpenAI API
              │             │
              └──────┬──────┘
                     ▼
                 AI Chatbot
```

---

## 🎯 Project Objectives

The main objectives of this project were to:

* Learn Telegram bot development with Python
* Integrate an external AI API
* Understand asynchronous programming
* Implement conversational AI
* Manage API credentials securely
* Build a real-world AI application
* Deploy an AI application to the cloud
* Practice Git and GitHub workflows

---

## 📚 What I Learned

Through this project, I gained practical experience with:

* Python application development
* Telegram Bot API
* Aiogram
* OpenAI API integration
* Environment variables
* `.env` security
* AsyncIO
* API-based AI applications
* Git and GitHub
* Cloud deployment with Railway

---

## 🔮 Future Improvements

Possible future improvements include:

* [ ] Persistent conversation history
* [ ] Database integration
* [ ] User authentication
* [ ] Multiple AI model support
* [ ] Streaming AI responses
* [ ] Image generation
* [ ] Voice message support
* [ ] Speech-to-text
* [ ] Text-to-speech
* [ ] Admin dashboard
* [ ] Usage tracking
* [ ] Rate limiting
* [ ] Improved error handling
* [ ] Docker support

---

## 🧪 Production Improvements

For a production-ready version, the project could be improved with:

* Database-backed conversation storage
* Proper logging
* Exception handling
* API rate limiting
* Monitoring
* Health checks
* Secure secret management
* User-level conversation sessions
* Automated deployment
* Unit and integration testing

---

## 📸 Project Demo

You can add screenshots of your Telegram chatbot here:

```text
docs/
├── start-command.png
├── ai-chat.png
└── clear-command.png
```

Then add them to the README:

```markdown
![MethzBot Start](docs/start-command.png)

![AI Conversation](docs/ai-chat.png)
```

---

## 🌟 Highlights

* Real-world AI application
* Telegram integration
* OpenAI API integration
* Asynchronous Python architecture
* Secure environment-variable configuration
* Cloud deployment ready
* GitHub portfolio project

---

## 👨‍💻 Author

**Sudeera Attanayake**

AI/ML Engineer in training focused on:

```text
Artificial Intelligence
Machine Learning
Deep Learning
Natural Language Processing
Generative AI
LLMs
RAG
AI Agents
MLOps
```

---

## 📄 License

This project is intended for **educational and portfolio purposes**.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

## 📌 Conclusion

**MethzBot** demonstrates how Python, Telegram, and modern AI APIs can be combined to create a practical conversational AI application.

The project provides hands-on experience with **AI API integration, asynchronous programming, secure configuration, GitHub development, and cloud deployment**, making it a strong foundation for further AI engineering projects.
