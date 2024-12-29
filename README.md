# 🚀 GPT-Resume: Your AI-Powered Resume Filtering App

Welcome to **GPT-Resume**, a cutting-edge application that seamlessly integrates **Django**, **Next.js**, and **OpenAI's GPT API** to revolutionize how resumes are analyzed and filtered! Whether you're hiring for your dream team or looking to streamline recruitment, GPT-Resume has your back! 🎯

---

## 🌟 Key Features

### 🧩 Backend (Django):
- **API Endpoints**: Upload resumes, post job descriptions, and retrieve filtered results with ease.
- **OpenAI GPT Integration**: Leverage the power of **GPT-3.5** or customize it with parameters for tailored analysis.
- **Database-Backed**: Store job postings, resume details, and results in a robust SQLite database.

### 🎨 Frontend (Next.js/React):
- **Intuitive UI**: Effortlessly upload resumes and post job descriptions.
- **Dynamic Results**: Get real-time results for the most relevant candidates.
- **Modern Design**: Built with reusable React components and state-of-the-art libraries.

### 💡 What It Does:
1. 📂 Upload resumes (PDFs).
2. 📝 Input job descriptions.
3. 🤖 Match resumes to job requirements using GPT's AI magic.
4. 🎯 Get the top candidates for your role!

---

## 🔧 Prerequisites

Before diving in, make sure you have these installed on your system:

| Tool         | Minimum Version |
|--------------|-----------------|
| **Python**   | 3.12.2          |
| **Git**      | 2.43.2          |
| **Node.js**  | 21.6.2          |
| **npm**      | 10.4.0          |

### 👉 Check your versions:
```bash
python --version
git --version
node --version
npm --version
```

---

## 🛠️ Setup Guide

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/akshanshbhatt/gpt-resume.git
cd gpt-resume
```

### 2️⃣ Create a Virtual Environment
```bash
python -m venv gpt-venv
```
- **Activate it**:
  - On Windows:
    ```bash
    .\gpt-venv\Scripts\activate
    ```
  - On macOS/Linux:
    ```bash
    source gpt-venv/bin/activate
    ```

### 3️⃣ Install Backend Dependencies
```bash
cd gpt_resume
python -m pip install -r requirements.txt
```

### 4️⃣ Set Up Environment Variables
Create a `.env` file in the root directory with the following content:
```plaintext
OAI_API_KEY = "<YOUR_OPENAI_API_KEY>"
DJANGO_SECRET_KEY = "<YOUR_DJANGO_SECRET_KEY>"
```
- Generate your Django secret key:
  ```bash
  python -c "from django.core.management.utils import get_random_secret_key; print(f'django-insecure-{get_random_secret_key()}')"
  ```

### 5️⃣ Migrate the Database
```bash
python manage.py makemigrations
python manage.py migrate
```

### 6️⃣ Run the Backend Server
```bash
python manage.py runserver
```
- Your server is now live at [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

### 7️⃣ Set Up the Frontend
```bash
cd ../gpt_resume_frontend
npm install
npm run dev
```
- Access the frontend at [http://127.0.0.1:3000/](http://127.0.0.1:3000/).

---

## 📂 Project Structure

### Backend:
- **`gpt_resume/`**: Django project settings and configuration.
- **`api/`**: Core application with models, views, and API logic.

### Frontend:
- **`gpt_resume_frontend/`**: Next.js-based frontend.
  - **`components/`**: Reusable UI components.
  - **`pages/`**: Page-based routing.

### Miscellaneous:
- **`sample_resume/`**: Example resumes for testing.
- **`.env`**: Stores your API keys and secrets.

---

## 🌐 API Endpoints

| Endpoint                          | Method | Description                                                |
|-----------------------------------|--------|------------------------------------------------------------|
| `/api/get-applicant-list/<uuid>`  | GET    | Fetches a list of applicants for a job posting.            |
| `/api/get-applicant-summary/<id>` | GET    | Retrieves a detailed summary of an applicant.              |
| `/api/post-resume/`               | POST   | Uploads resumes for analysis.                              |
| `/api/post-job/`                  | POST   | Creates a new job posting.                                 |
| `/api/post-resume-with-job/`      | POST   | Combines job creation and resume analysis in one request.  |

---

## 🧪 Sample Testing

1. Upload resumes from the `sample_resume/` folder.
2. Post a job description.
3. Fetch the matched candidates from the API or view results on the frontend.

---

## 🎉 Let’s Get Started!
Whether you’re a recruiter, developer, or AI enthusiast, **GPT-Resume** empowers you to streamline resume filtering like never before. 🚀 Start today and experience the future of hiring!

---

## 🤝 Contributing
We welcome contributions! Feel free to fork the repository, create a feature branch, and submit a pull request. 🙌


---

## ✨ External Resources
- **Sample Resumes**: [CMU Career Center](https://www.cmu.edu/career/documents/sample-resumes-cover-letters/sample-resumes_scs.pdf)
- **OpenAI API**: [OpenAI Documentation](https://platform.openai.com/docs/)
