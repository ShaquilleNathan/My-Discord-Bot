# 🤖 Discord Bot

A simple Python-based Discord bot that can greet users and send random quotes along with emojis. Built using the `discord.py` library, this bot is ideal for beginners who want to explore the basics of Discord bot development.

---

## ✨ Features

- Responds to greetings using commands like `/hello` or `$hello`.
- Sends a collection of emojis using `/emoji` or `$emoji`.
- Displays a random inspirational quote with `/inspire` or `$inspire`.
- Easy to customize: you can add your own commands and responses in the source code.

---

---

## 💡 Commands Guide

| Command            | Description                         |
|--------------------|-------------------------------------|
| `/hello` or `$hello` | Bot sends a greeting message       |
| `/emoji` or `$emoji` | Bot sends a list of emojis         |
| `/inspire` or `$inspire` | Bot replies with a random quote    |

All command triggers can be customized easily in the `main.py` file by modifying the `on_message` function.

---

## 🚀 How to Run This Discord Bot (Python)

Follow these steps carefully to set up and run your bot:

### 1. Clone the Repository
```bash
git clone //this repo link
cd your-bot-repo
```
### 2. Install Required Libraries
Make sure Python is installed (recommended: Python 3.8+), then install the required packages:
```bash
pip install discord.py python-dotenv
```
### 3. Create a Bot via Discord Developer Portal
- Visit: https://discord.com/developers/applications
- Click New Application, name it (e.g. MyBot)
- Go to the Bot tab → click Add Bot
- Under Bot settings, enable the "Message Content Intent"
- Copy the bot token that has been sent in a `.txt` extension (you’ll use this in the next step)
### 4. Store Your Token Securely
Create a .env file in your project directory:
```ini
DISCORD_BOT_TOKEN=your_real_token_here
```
Ensure your main.py reads the token like this:
```python
import os
from dotenv import load_dotenv

load_dotenv()
TOKEN = os.getenv("DISCORD_BOT_TOKEN")
client.run(TOKEN)
```
### 5. Invite Bot to Your Discord Server
- Go to the OAuth2 > URL Generator menu
- Select:
  1) Scopes: bot
  2) Bot Permissions: Send Messages, Read Message History
- Copy the generated URL, paste it in your browser, and invite the bot to your server
### 6. Run the Bot
In your terminal or editor:
```bash
python main.py
```
You should see output like:
```csharp
We have logged in as GreetingsBot#1234
```
### 🧠 Example Output
```vbnet
User: $hello
Bot: Hello there! 👋

User: /emoji
Bot: 😄 🤖 🚀 🐍 🧠 🎉

User: /inspire
Bot: "The only limit to our realization of tomorrow is our doubts of today." – Franklin D. Roosevelt
```

<div align="center">
  <img src="https://i.postimg.cc/TPRs9frD/Whats-App-Image-2025-05-17-at-17-50-35.jpg" alt="Demo Image" style="width: 500px; height: auto;" />
  <img src="https://i.postimg.cc/2jsrxL3L/Whats-App-Image-2025-05-17-at-17-51-09.jpg" alt="Demo Image" style="width: 500px; height: auto;" />
</div>

### 📌 Notes
- The bot is experimental and can be improved further.
- The quotes are selected from a predefined list (can be connected to API later).
- All commands are case-sensitive and can be extended easily.

