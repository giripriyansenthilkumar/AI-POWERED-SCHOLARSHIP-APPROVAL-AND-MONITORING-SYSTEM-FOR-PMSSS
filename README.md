# AI Portal

This project is a web application built with Django and Node.js, designed to handle user registration, applicant data collection, family and bank details, and more. It features a multi-step form process and integrates both backend and frontend technologies.

## Features
- User registration and login
- Multi-step applicant form (personal, family, and bank details)
- File uploads for supporting documents
- RESTful endpoints for form submissions
- Basic frontend templates for user interaction
- Node.js microservice (in `mynodejsservice/`)

## Project Structure
```
aiportal_updated/
├── aiportal/           # Django project settings and configuration
├── aippapp/            # Main Django app with models, views, forms, templates, static files
│   ├── migrations/
│   ├── static/
│   ├── templates/
│   └── ...
├── mynodejsservice/    # Node.js microservice (optional)
├── db.sqlite3          # SQLite database
├── manage.py           # Django management script
├── package.json        # Node.js dependencies (if any)
```

## Setup Instructions

### Prerequisites
- Python 3.10+
- Node.js (for `mynodejsservice`)
- pip (Python package manager)

### Python/Django Setup
1. **Install dependencies:**
   ```sh
   pip install django
   ```
2. **Apply migrations:**
   ```sh
   python manage.py migrate
   ```
3. **Run the development server:**
   ```sh
   python manage.py runserver
   ```
4. **Access the app:**
   Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

### Node.js Service (Optional)
1. Navigate to `mynodejsservice/`:
   ```sh
   cd mynodejsservice
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the Node.js server:
   ```sh
   node server.js
   ```

## Main Django App URLs
- `/` : Home page
- `/login/` : Login page
- `/register/` : Registration page
- `/app1/` : Applicant details form
- `/app2/` : Family details form
- `/app3/` : Bank details form
- `/app4/` : Final step/confirmation

## File Uploads
- Family and bank details forms support file uploads (e.g., ITR, bank statements).
- Uploaded files are handled via Django forms and models.

## Customization
- Update templates in `aippapp/templates/aippapp/` for UI changes.
- Static files (CSS/JS) are in `aippapp/static/`.
- Add or modify models in `aippapp/models.py` as needed.

## License
This project is for educational/demo purposes. Please add a license if you intend to use it in production.
