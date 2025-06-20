#  Superheroes API

This is a Flask RESTful API for managing superheroes and their powers. The app supports full CRUD operations, including viewing heroes, powers, and creating new hero-power relationships. It also validates data and sends an email notification whenever a hero gains a new power.

#  Features
- View all heroes and powers
- Get details of a single hero or power
- Update a power's description
- Create a new hero-power relationship
- Email notification sent upon successful hero-power creation

# Getting Started

# Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/superheroes-api.git
cd superheroes-api
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Set up the database:

```bash
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
```

4. (Optional) Seed the database with sample data:

```bash
python seed.py
```

5. Run the app:

```bash
flask run
```

# API Endpoints

**GET /heroes** – returns all heroes

**GET /heroes/<id>** – returns a hero with nested hero powers

**GET /powers** – returns all powers

**GET /powers/<id>** – returns a single power

**PATCH /powers/<id>** – updates the description of a power

**POST /hero_powers** – assigns a new power to a hero

See the source code for the full request/response examples.

# Email

Configure your email credentials in `app.config`:

```python
app.config['MAIL_USERNAME'] = 'your_mailtrap_username'
app.config['MAIL_PASSWORD'] = 'your_mailtrap_password'
```

