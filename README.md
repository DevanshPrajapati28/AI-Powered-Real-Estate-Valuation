# 🏡 StreetBase – AI-Powered Real Estate Valuation Platform

**An intelligent real estate platform that combines machine learning, property analytics, and interactive tools to simplify property valuation and real estate decision-making.**

StreetBase is a Python-based real estate application designed to provide users with an interactive platform for exploring property information and estimating property values.

The project integrates machine learning, data visualization, and AI-assisted features into a user-friendly Streamlit application.

---

## 🚀 Key Features

### 🏠 Property Valuation
- Estimate property prices using a machine learning-based valuation system.
- Analyze property-related information and input features.
- Provide an interactive property valuation experience.

### 📊 Interactive Dashboard
- User-friendly and responsive Streamlit interface.
- Organized navigation across multiple application sections.
- Interactive property-related information and visual elements.

### 🤖 AI Chatbot Interface
- Integrated chatbot interface for AI-assisted user interaction.
- Designed to support users navigating real estate-related information.

### 🏢 Real Estate Services
- Dedicated services section.
- Case studies and real estate-related information.
- News and informational content.

### 💰 EMI Calculator
- Calculate estimated loan installments.
- Explore property financing scenarios.

### ❤️ User Features
- Sign-in interface.
- Property favourites section.
- Dedicated navigation and user interaction components.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend / UI | Streamlit |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Data Visualization | Plotly, Matplotlib, Seaborn |
| AI / NLP Dependencies | OpenAI, Transformers, Sentence Transformers |
| Deep Learning | PyTorch |
| PDF Processing | PyPDF2 |
| Image Processing | Pillow |
| Model Persistence | Joblib |
| Version Control | Git, GitHub |

---

## 🏗️ Application Architecture

StreetBase follows a modular architecture in which the main Streamlit application manages navigation and integrates different components and pages.

```text
                  ┌──────────────────────┐
                  │        User          │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │  Streamlit Frontend  │
                  │       app.py         │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │   Navigation System  │
                  │     & Components     │
                  └──────────┬───────────┘
                             │
             ┌───────────────┼────────────────┐
             │               │                │
             ▼               ▼                ▼
      ┌────────────┐  ┌─────────────┐  ┌─────────────┐
      │  Property  │  │   Services  │  │  Case       │
      │  Valuation │  │   & News    │  │  Studies    │
      └─────┬──────┘  └─────────────┘  └─────────────┘
            │
            ▼
      ┌──────────────┐
      │ ML / Data    │
      │ Processing   │
      └──────┬───────┘
             │
             ▼
      ┌──────────────┐
      │  Prediction  │
      │  & Results   │
      └──────────────┘

       Additional Modules:
       • AI Chatbot Interface
       • EMI Calculator
       • User Authentication
       • Favourites Management
```

---

## 📂 Project Structure

```text
AI-Powered-Real-Estate-Valuation/
│
├── Assets/
│   └── Images and static resources
│
├── backend/
│   └── api/
│       └── Backend API modules
│
├── components/
│   ├── NavBar/
│   │   └── navbar.py
│   ├── Hero/
│   ├── chatbot_ui.py
│   ├── simple_app.py
│   └── features.py
│
├── data/
│   └── Dataset and application data
│
├── login/
│   └── Authentication modules
│
├── pages/
│   ├── services.py
│   ├── case_studies.py
│   ├── news.py
│   ├── AboutUs.py
│   ├── Signin.py
│   ├── emi_calc.py
│   └── favourites.py
│
├── utils/
│   └── Utility modules
│
├── app.py
├── Signin.py
├── StreetBase_KB.pdf
├── news_classifier_model.joblib
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Installation and Setup

Follow these steps to run StreetBase locally.

### 1. Clone the Repository

```bash
git clone https://github.com/DevanshPrajapati28/AI-Powered-Real-Estate-Valuation.git
```

Navigate to the project directory:

```bash
cd AI-Powered-Real-Estate-Valuation
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate the environment on Windows:

```bash
.venv\Scripts\activate
```

For macOS / Linux:

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

Install the required packages:

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

If your local configuration requires API credentials, create a `.env` file in the project root.

Add the environment variables required by the corresponding application modules.

**Important:** Never commit API keys, passwords, or other sensitive credentials to GitHub.

### 5. Run the Application

Start the Streamlit application using:

```bash
streamlit run app.py
```

The application will generally open at:

```text
http://localhost:8501
```

---

## 🔄 Application Workflow

1. **Launch Application:** Start StreetBase through the Streamlit entry point.
2. **Navigate:** Explore the different sections through the custom navigation bar.
3. **Property Valuation:** Access the property valuation section and provide the required property information.
4. **Prediction:** Use the configured machine learning workflow to estimate property value.
5. **Explore Features:** Access services, case studies, news, and other real estate information.
6. **Calculate EMI:** Use the EMI calculator to estimate loan installments.
7. **Interact:** Explore the chatbot interface and other available application features.

---

## 📈 Machine Learning Approach

The project focuses on applying machine learning techniques to real estate valuation.

The general machine learning workflow includes:

- Data collection and dataset preparation.
- Data cleaning and preprocessing.
- Exploratory Data Analysis (EDA).
- Feature engineering.
- Model training and evaluation.
- Property price prediction.

Model evaluation can be performed using regression metrics such as:

- R² Score
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

---

## 🔮 Future Enhancements

- Improve property valuation accuracy through advanced machine learning models.
- Add location-based property price analysis.
- Integrate interactive geographical property visualizations.
- Enhance AI chatbot capabilities with Retrieval-Augmented Generation (RAG).
- Introduce personalized property recommendations.
- Implement secure user authentication and persistent user preferences.
- Deploy the application to a cloud platform.

---

## ⚠️ Disclaimer

StreetBase is an educational and experimental real estate technology project.

Property valuations are estimates generated using available data and configured models. They should not be considered official property appraisals, financial advice, or guaranteed market prices.

Actual property values may vary depending on location, market conditions, property characteristics, and other factors.

---

## 👨‍💻 Author

**Devansh Prajapati**

B.Tech – Information Technology

- GitHub: [@DevanshPrajapati28](https://github.com/DevanshPrajapati28)
- LinkedIn: [Devansh Prajapati](https://www.linkedin.com/in/devansh-prajapati-180b3a285/)

---

⭐ If you find this project interesting, consider giving the repository a star!

**Built with Python, Machine Learning, and Streamlit.**
