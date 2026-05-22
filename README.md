# 🤖 ChatterBot Flask — AI Chatbot with Wikipedia Fallback

A conversational AI chatbot built with **Flask** and **ChatterBot**, featuring YAML-based training data across multiple topics and an intelligent Wikipedia fallback for unknown queries. Includes voice input and text-to-speech output.

---

## ✨ Features

- **Multi-Topic Training** — Trained on 15+ YAML datasets covering AI, politics, history, food, humor, sports, and more
- **Wikipedia Fallback** — When confidence is low, automatically fetches answers from Wikipedia
- **Voice Input** — Speech-to-text support via Web Speech API
- **Text-to-Speech** — Bot responses are spoken aloud using the browser's SpeechSynthesis API
- **Real-Time Chat UI** — Responsive chat panel with color-coded messages (green for user, white for bot)
- **Confidence Threshold** — Only returns trained responses when confidence exceeds 10%

## 🛠️ Tech Stack

| Layer      | Technology                          |
|------------|-------------------------------------|
| Backend    | Python, Flask                       |
| AI Engine  | ChatterBot, ListTrainer             |
| NLP        | spaCy, NLTK                         |
| Scraping   | BeautifulSoup4, Requests            |
| Frontend   | HTML, Bootstrap 3, jQuery           |
| Database   | SQLite (ChatterBot default storage) |

## 📁 Project Structure

```
chatterbot-flask-2020/
├── chatbot.py              # Main Flask app with ChatterBot + Wikipedia fallback
├── requirments.txt         # Python dependencies
├── db.sqlite3              # ChatterBot SQLite database
├── data/                   # YAML training datasets
│   ├── ai.yml
│   ├── botprofile.yml
│   ├── computers.yml
│   ├── conversations.yml
│   ├── emotion.yml
│   ├── food.yml
│   ├── gossip.yml
│   ├── greetings.yml
│   ├── history.yml
│   ├── humor.yml
│   ├── literature.yml
│   ├── money.yml
│   ├── politics.yml
│   ├── psychology.yml
│   ├── sports.yml
│   └── trivia.yml
└── templates/
    └── chat.html           # Chat UI with voice support
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- pip

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/chatterbot-flask-2020.git
cd chatterbot-flask-2020

# Install dependencies
pip install -r requirments.txt

# Run the application
python chatbot.py
```

The app will start at `http://127.0.0.1:5000/`

## 💬 How It Works

1. User sends a message via the chat interface
2. ChatterBot checks its trained data for a matching response
3. If confidence > 10% → returns the trained response
4. If the message is "bye" → returns a farewell message
5. Otherwise → scrapes Wikipedia for an answer
6. If Wikipedia fails → returns a fallback "no idea" response

## 📸 Preview

The chat interface features a dark-themed panel with:
- Color-coded messages (green = user, white = bot)
- Send, Clear, and Voice buttons
- Auto-scroll to latest messages

---
