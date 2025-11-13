
# 📝 Flask Blog

A fully functional blog application built using **Flask**, **Flask-Mail**, **SQLAlchemy**, and **Bootstrap**.

---

## Features
- User registration & login (with hashed passwords)
- Post creation, editing, deletion
- Password reset via email
- SQLAlchemy ORM + Flask-Migrate support
- Bootstrap 5 UI
- Secure environment variables via `.env`

---

## Project Structure

```
Flask_Blog/
│
├── flaskblog/
│   ├── __init__.py
│   ├── models.py
│   ├── routes.py
│   ├── forms.py
│   ├── templates/
│   └── static/
│
├── instance/
│   └── site.db
│
├── .env
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Installation

### Clone the repository
```bash
git clone https://github.com/<your-username>/<repo>.git
cd <repo>
```

### Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
.\.venv\Scripts\activate     # Windows
```

### Install packages
```bash
pip install -r requirements.txt
```

---

## Environment Variables (.env)

```
SECRET_KEY=your_flask_secret_key
SQLALCHEMY_DATABASE_URI=sqlite:///site.db

EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
```

Use **Gmail App Password**, not your login password.

---

## Run the App
```bash
flask run
```

---

## Security Notes
- `.env` is already in `.gitignore`
- Never push secrets to GitHub
- Rotate App Password if exposed

---

## Email Setup
Configured using Gmail SMTP:

```python
app.config['MAIL_SERVER'] = 'smtp.gmail.com'
app.config['MAIL_PORT'] = 587
app.config['MAIL_USE_TLS'] = True
app.config['MAIL_USERNAME'] = os.environ.get('EMAIL_USER')
app.config['MAIL_PASSWORD'] = os.environ.get('EMAIL_PASS')
```

---

## License
MIT License © 2025
