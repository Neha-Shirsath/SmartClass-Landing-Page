# SnapClass – Making Attendance Faster Using AI

SnapClass is an **AI-powered attendance management system** that automates classroom attendance using facial recognition. It helps teachers reduce the time spent on manual attendance while maintaining digital attendance records.

🔗 **Live Demo:** https://snapclass-main-byneha.streamlit.app/



## 📌 Table of Contents

* [Overview](#-overview)
* [Features](#-features)
* [How It Works](#-how-it-works)
* [Technology Stack](#-technology-stack)
* [Project Structure](#-project-structure)
* [Installation](#-installation)
* [Configuration](#-configuration)
* [Usage](#-usage)
* [Database](#-database)
* [Deployment](#-deployment)
* [Future Improvements](#-future-improvements)
* [Author](#-author)

---

## 🔎 Overview

Traditional attendance is often time-consuming and requires teachers to manually record each student's presence.

**SnapClass** uses AI-based facial recognition to identify registered students and automatically record their attendance.

The application is built with **Python and Streamlit** and uses a database to store student and attendance information.

### 🎯 Goals

* Reduce the time required for classroom attendance
* Automate student identification
* Maintain digital attendance records
* Provide a simple teacher-friendly interface
* Reduce errors associated with manual attendance

---

## ✨ Features

### 👩‍🏫 Teacher

* Teacher registration and login
* Create and manage subjects
* Generate subject join codes
* View enrolled students
* Capture classroom images
* Automatically recognize registered students
* Mark attendance
* View attendance records

### 👨‍🎓 Student

* Student registration and login
* Register facial information
* Join subjects using a join code
* View enrolled subjects
* View attendance records

### 🤖 AI Features

* Face detection
* Facial feature extraction
* Face embedding generation
* Student identification using machine learning
* Automated attendance marking

---

## ⚙️ How It Works

```text
                    ┌───────────────────┐
                    │      SnapClass    │
                    │    Streamlit UI   │
                    └─────────┬─────────┘
                              │
                 ┌────────────┴────────────┐
                 │                         │
          ┌──────▼──────┐           ┌─────▼──────┐
          │   Teacher   │           │  Student   │
          │    Portal   │           │   Portal   │
          └──────┬──────┘           └─────┬──────┘
                 │                        │
                 └───────────┬────────────┘
                             │
                    ┌────────▼────────┐
                    │  Face Detection │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │ Face Embeddings │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │ ML Classification│
                    │      (SVM)      │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │ Student         │
                    │ Identification  │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │ Attendance      │
                    │ Recorded        │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │    Database     │
                    └─────────────────┘
```

### Face Recognition Pipeline

```text
Student Face
     ↓
Face Detection
     ↓
Face Embedding
     ↓
SVM Classification
     ↓
Student Identification
     ↓
Attendance Recorded
```

---

## 🛠️ Technolitogy Stack

### Frontend

* **Streamlit**

### Programming Language

* **Python**

### AI / Machine Learning

* **Dlib**
* **face_recognition**
* **Scikit-learn**
* **SVM**
* **NumPy**

### Data Processing

* **Pandas**

### Database

* **Supabase**
* **PostgreSQL**

### Authentication & Security

* **bcrypt**
* Streamlit Secrets

### Deployment

* **Streamlit Community Cloud**

### Version Control

* **Git**
* **GitHub**

---

## 📂 Project Structure

```text
SnapClass/
│
├── app.py
├── requirements.txt
├── README.md
│
├── screens/
│   ├── home_screen.py
│   ├── student_screen.py
│   └── teacher_screen.py
│
├── pipelines/
│   └── face_pipeline.py
│
├── database/
│   └── database_functions.py
│
├── ui/
│   └── base_layout.py
│
└── .streamlit/
    └── secrets.toml
```

> The project structure may vary depending on the current version of the repository.

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Neha-Shirsath/Snapclass-by-Neha_Shirsath.git
```

### 2. Navigate to the Project

```bash
cd Snapclass-by-Neha_Shirsath
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Configuration

SnapClass uses **Supabase** for database operations.

Create a Streamlit secrets file:

```text
.streamlit/
└── secrets.toml
```

Add your credentials:

```toml
SUPABASE_URL = "your_supabase_url"
SUPABASE_KEY = "your_supabase_key"
```

### ⚠️ Security

Never commit your `secrets.toml` file or expose database/API credentials publicly.

Add it to `.gitignore`:

```text
.streamlit/secrets.toml
```

---

## ▶️ Usage

Run the Streamlit application:

```bash
streamlit run app.py
```

The application will start locally and can be accessed through the URL shown in the terminal.

---

## 🗄️ Database

SnapClass uses **Supabase/PostgreSQL** to store application data.

The database manages information such as:

* Student details
* Teacher details
* Subjects
* Student enrollment
* Face embeddings
* Attendance records

---

## ☁️ Deployment

The application is deployed using **Streamlit Community Cloud**.

### Live Application

🔗 https://snapclass-main-byneha.streamlit.app/

---

## 🔮 Future Improvements

* Real-time camera-based attendance
* Face liveness detection
* Improved recognition under different lighting conditions
* Attendance analytics and visual dashboards
* Automated attendance reports
* Email notifications for attendance
* Mobile-friendly interface
* Improved scalability for large classrooms


## 📊 Key Learning Outcomes

Through this project, I worked with:

* AI-based face recognition
* Face embeddings
* Machine learning classification
* Streamlit application development
* Database integration
* Authentication
* Git and GitHub
* Cloud deployment
* Handling sensitive credentials securely

---

## 👩‍💻 Author
### Neha Shirsath


