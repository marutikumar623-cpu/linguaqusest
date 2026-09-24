# LinguaQuest — Flask Online + Gemini AI

LinguaQuest is a Flask-based student learning web app with online accounts, cloud-ready server data, a Gemini 2.5 Flash learning assistant, and student feedback.

## Features
- Online signup/login with server-side password hashing
- Student profile and saved LinguaQuest state in SQLite
- 🤖 Gemini 2.5 Flash AI Assistant
  - Assignment helper
  - Difficult-topic explanations
  - Step-by-step Maths solving
  - General study help
- 💬 Student feedback with 1–5 star rating
- Existing quizzes, XP, habits, study timer, health and sports features

## Setup

1. Create a Gemini API key in Google AI Studio.
2. Set the API key as an environment variable. **Do not put the key in `index.html`.**

Windows PowerShell:
```powershell
$env:GEMINI_API_KEY="YOUR_API_KEY"
$env:SECRET_KEY="YOUR_RANDOM_SECRET"
```

Windows CMD:
```cmd
set GEMINI_API_KEY=YOUR_API_KEY
set SECRET_KEY=YOUR_RANDOM_SECRET
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Start the server:
```bash
python app.py
```

5. Open:
```text
http://127.0.0.1:5000/
```

## Important for public deployment
- Set `GEMINI_API_KEY` and a strong `SECRET_KEY` in the hosting provider's environment variables.
- Do not commit or share the API key.
- Use HTTPS in production.
- Flask's built-in development server is for development/testing, not production hosting.

The AI endpoint uses the stable model name `gemini-2.5-flash` on the Flask server, so the API key is never exposed to the browser.
