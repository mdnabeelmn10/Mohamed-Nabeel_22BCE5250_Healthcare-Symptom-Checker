# 🏥 Healthcare Symptom Checker

A full-stack web application that allows users to input symptoms and receive **educational suggestions** about possible conditions and next steps — powered by **Google Gemini API**.  

> ⚠️ This tool is for **educational purposes only** and is **not a substitute for professional medical advice or diagnosis**.

---

## 🚀 Features

- **Symptom Input Form** — Users can describe their symptoms in plain text.  
- **LLM-powered Reasoning** — The backend queries Gemini to generate probable conditions and safe recommendations.  
- **Safety First** — Every response includes a clear disclaimer.  
- **Query Logging (Optional)** — Each request can be stored in a database for analytics or history.  
- **Responsive UI** — Simple, modern React interface styled with CSS.

---

## 🧩 Tech Stack

| Component | Technology |
|------------|-------------|
| **Frontend** | React (Create React App) |
| **Backend** | Django + Django REST Framework |
| **LLM Integration** | Google Gemini API |
| **Database** | SQLite (default) |
| **Styling** | Plain CSS |

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/healthcare-symptom-checker.git
cd healthcare-symptom-checker
```

---

### 2. Backend Setup (Django)

```bash
cd backend
python -m venv venv
source venv/bin/activate     # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Create a `.env` file inside the `backend` folder:

```
GEMINI_API_KEY=your_gemini_api_key_here
```

Run migrations and start the Django server:

```bash
python manage.py migrate
python manage.py runserver
```

Your backend will be live at  
👉 `http://127.0.0.1:8000/api/symptom-checker/`

---

### 3. Frontend Setup (React)

```bash
cd frontend
npm install
npm start
```

Your frontend will run at  
👉 `http://localhost:3000`

---

## 🔗 API Endpoint

**POST** `/api/symptom-checker/`

### Request:

```json
{
  "symptom": "I have a sore throat, mild fever, and cough."
}
```

### Response:

```json
{
  "condition": "Possible common cold or mild viral infection",
  "recommendation": "Stay hydrated, rest, and consult a doctor if fever persists beyond 3 days.",
  "disclaimer": "This is for educational purposes only and should not be considered medical advice."
}
```

---

## 🧠 Gemini API Integration

The Django backend sends user symptoms to Gemini with a prompt like:

> “Based on these symptoms, suggest possible conditions and next steps with an educational disclaimer.”

Make sure your `.env` file includes:

```
GEMINI_API_KEY=your_key_here
```

---

## 🧪 Example Flow

1. Open `http://localhost:3000`  
2. Enter your symptoms (e.g., “I have a sore throat and headache.”)  
3. Click **Submit**  
4. View probable conditions and safe recommendations (with disclaimer)

---

## 🧷 Safety & Ethics

* The output is **educational** and should **not replace professional consultation**.  
* All responses are accompanied by a **medical disclaimer**.  
* No personal health data is shared or stored unless you explicitly enable logging.

---

## 🧑‍💻 Author

**Mohamed Nabeel**  
💻 B.Tech CSE Core @ VIT Chennai | B.Sc Data Science @ IIT Madras  
📊 Passionate about Data Science & AI-based applications

---

## 📜 License

This project is released under the **MIT License** — feel free to modify and use it responsibly.
