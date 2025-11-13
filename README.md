📝 Flask Blog

A fully functional blog application built using Flask, Flask-Mail, SQLAlchemy, and Bootstrap.
It supports user registration, login, post creation/editing/deletion, password reset via email, and more.

Features

User registration & login (with hashed passwords)

Create, update, delete blog posts

Pagination for posts

Password reset via email (Flask-Mail)

Flash messages & form validations

Templates using Bootstrap 5

SQLAlchemy ORM with relational models

Secure environment variable management via .env

📁 Project Structure
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

Installation & Setup
Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
.\.venv\Scripts\activate       # Windows

Install dependencies
pip install -r requirements.txt

Environment Variables (Create .env file)

Create a .env file in the project root:

SECRET_KEY=your_flask_secret_key

# Database connection URI
SQLALCHEMY_DATABASE_URI=sqlite:///site.db
# Or: postgresql://user:password@localhost/dbname

# Email credentials
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_generated_app_password



Always keep these values secret



Gmail requires:

2-Step Verification ON

App Password generated for “Mail” → “Other (Flask)”

Database Setup

To initialize the database:

flask shell


Then inside the shell:

from flaskblog import db
db.create_all()

Running the Application
flask run


App runs at:

http://127.0.0.1:5000


Security Notes

Do NOT push .env or secrets to GitHub.

Rotate email app password if exposed.

Use a test SMTP service (Mailtrap/Ethereal) during development.


License

This project is open source under the MIT License.