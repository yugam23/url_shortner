# 🚀 URL Shortner

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) [![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/) [![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](https://github.com/)

**A tiny, easy-to-use URL shortener built with Flask and SQLite.**

---

## 💡 Overview

This project provides a minimal web app that shortens long URLs and redirects requests from the generated short path to the original URL. It uses Flask for the web app and SQLAlchemy + SQLite for persistence.

- Tech: **Python**, **Flask**, **Flask-SQLAlchemy**, **SQLite**
- Files of interest: `run.py`, `templates/index.html`, `templates/result.html`

---

## ⚙️ Features

- Generate short, random URLs (default length: 6)
- Store mappings in a local SQLite database (`links.db`)
- Simple HTML form UI to create short links

---

## 🧩 Quick Start

### Prerequisites

- Python 3.8+ installed
- Git (optional)

### 1) Clone or open the project

If you cloned the repo:

```bash
git clone <repo-url>
cd "Url Shortner"
```

> Note: this repo already contains a `requirements.txt` file.

### 2) Create and activate a virtual environment

Windows (PowerShell):

```powershell
python -m venv env
env\Scripts\Activate.ps1
```

Windows (cmd.exe):

```cmd
python -m venv env
env\Scripts\activate.bat
```

macOS / Linux:

```bash
python3 -m venv env
source env/bin/activate
```

### 3) Install dependencies

```bash
pip install -r requirements.txt
```

### 4) Run the app

```bash
python run.py
```

Open your browser at: http://127.0.0.1:5000

---

## 🧪 Details / Notes

- The app uses `sqlite:///links.db` by default. The database file `links.db` is automatically created on first run.
- Short codes are 6 characters (letters + digits) by default. You can change `gen_short(length=6)` in `run.py` if you want different lengths.
- To run in development mode with auto-reload, set `FLASK_ENV=development` and run with `flask run` or edit `run.py` to `app.run(debug=True)` (for convenience during development).

---

## 🛠️ Project Structure

```
Url Shortner/
├─ run.py            # Flask app and URL model
├─ requirements.txt  # Dependencies
├─ templates/
│  ├─ index.html
│  └─ result.html
├─ instance/         # Flask instance folder (if used)
└─ links.db          # SQLite DB (created at runtime)
```

---

## ✅ Usage Example

1. Open the home page and paste a long URL into the form.
2. Click the button to shorten; the result shows a clickable shortened URL (e.g. `http://127.0.0.1:5000/Ab4kX2`).
3. Visiting that short path will redirect to the original long URL.

---

## 🤝 Contributing

- Feel free to open issues or PRs.
- Suggestions: add analytics, custom aliases, admin UI, rate limits, or tests.

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

Happy shortening! ✂️
