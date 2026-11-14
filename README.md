# 🏡 AI-Powered Real Estate Valuation

An interactive machine-learning application that estimates property prices using property characteristics such as location, property type, area, rooms, age, floor details, and amenities. The project provides a Streamlit interface where users can enter property information and view an estimated valuation with supporting visualisations.

> **Project information source:** The model and application details below are based on the project's supplied `STREAMLIT_INSTRUCTIONS.md`. Items not specified in that file are identified as details to verify rather than assumed.

## ✨ Features

### Property details
- Choose a location from the supported major Indian cities.
- Select a property type: Apartment, Villa, House, Plot, or Commercial.
- Enter the property area (sq. ft. or sq. m).
- Provide bedroom and bathroom counts.
- Enter the property's age or year built.
- Specify the floor number and total floors.
- Select applicable amenities.

### Valuation results
- Predicted property price displayed in ₹ Lakhs.
- Automatically calculated price per sq. ft.
- Indicative price range around the prediction.
- Interactive price-range charts.
- Comparable-property information.

### User interface
- Built with Streamlit.
- Responsive layout for desktop and mobile.
- Clean input form and real-time prediction experience.
- Navy blue (`#003366`) and orange (`#FF6600`) brand colours.

## 🤖 Machine Learning Model

According to the supplied project setup documentation, the application uses a **Gradient Boosting Regressor**.

| Model detail | Documented value |
|---|---|
| Regression algorithm | Gradient Boosting Regressor |
| R² score | 95.96% (as stated in the supplied setup notes) |
| RMSE | Approximately ₹2.93 Lakhs |
| Training data size | 250,000+ property records |
| Prediction target | Property price |
| Input features | Location, property type, area, age, rooms, floor details, amenities, and related property attributes |

### Evaluation notes

The supplied setup notes report an R² score of **99.96%** and an RMSE of approximately **₹2.93 Lakhs**. These are the values documented for the project; the setup notes do not include the train/test split, validation method, or a full evaluation report.

For a complete, reproducible model evaluation, add the following information from the model-training code or experiment results:
- Training and test split (or cross-validation strategy).
- R² score on the held-out test set.
- RMSE and MAE on the held-out test set.
- Any comparison with other regression algorithms, if they were actually trained.

Do not interpret the R² score as classification accuracy. The predicted value and indicative price range are estimates, not a guarantee of market value.

## 🔄 Dataset and Prediction Workflow

The supplied setup notes describe a training dataset of **250,000+ property records**. They do not identify the dataset's public source, download URL, exact columns, or detailed preprocessing steps. Add those details once confirmed from the dataset and training code.

The documented application workflow is:

1. **Enter property information** – Choose location and property type, then provide area, rooms, age, floor details, and amenities.
2. **Prepare model inputs** – The property characteristics are used as prediction features.
3. **Generate valuation** – The Gradient Boosting Regressor is documented as the model used to estimate the property price.
4. **Display the result** – The application presents the estimated price in ₹ Lakhs and calculates price per square foot.
5. **Explore supporting information** – Users can view the indicative price range, interactive charts, and comparable-property information.

### Workflow at a glance

```text
Property details
      |
      v
Input features
(location, type, area, rooms, age, floor, amenities)
      |
      v
Gradient Boosting Regressor
      |
      v
Estimated property price
      |
      v
Price per sq. ft. + indicative range + visualisations
```

## 🛠️ Technology Stack

The supplied setup notes explicitly mention these application and data-science packages:

- **Language:** Python
- **Web application:** Streamlit
- **Data handling:** Pandas, NumPy
- **Visualisation:** Plotly, Matplotlib, Seaborn
- **Machine learning:** Scikit-learn

The setup notes also list Streamlit, Pandas, NumPy, Plotly, Scikit-learn, Matplotlib, and Seaborn as installation dependencies. Refer to `requirements.txt` for the repository's full dependency list.

## 📁 Project Structure

The repository's application files may evolve. The setup instructions identify the following application entry points and launch helpers:

```text
AI-Powered-Real-Estate-Valuation/
│
├── app.py                           # Main Streamlit application entry point
├── property_valuation_app_simple.py # Simple Streamlit app entry point (setup notes)
├── start_app.py                     # Launcher script (setup notes)
├── run_streamlit.bat                # Windows launcher (setup notes)
├── requirements.txt                 # Python dependencies
├── STREAMLIT_INSTRUCTIONS.md        # Application setup instructions
└── ...
```

The setup notes mention both `app.py` and `property_valuation_app_simple.py` as possible Streamlit entry points. Use the entry point that matches the version of the application you intend to run. The repository's current `app.py` is used in the primary instructions below.

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/DevanshPrajapati28/AI-Powered-Real-Estate-Valuation.git
cd AI-Powered-Real-Estate-Valuation
```

### 2. Create a virtual environment (recommended)

**Windows – PowerShell**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If PowerShell prevents script activation, use Command Prompt:

```bat
.venv\Scripts\activate.bat
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If you only want to install the packages listed in the supplied quick-start instructions for the simple Streamlit app, use:

```bash
pip install streamlit pandas numpy plotly scikit-learn matplotlib seaborn
```

### 4. Run the application

From the repository root:

```bash
streamlit run app.py
```

The setup notes also describe these alternative launch methods for the simple app:

```bash
python start_app.py
```

or:

```bash
streamlit run property_valuation_app_simple.py
```

On Windows, you can also run:

```bat
run_streamlit.bat
```

### 5. Open the application

Once Streamlit starts, open the local URL shown in your terminal. The default is:

```text
http://localhost:8501
```

To use another port:

```bash
streamlit run app.py --server.port 8502
```

## 🖼️ Application Screenshots

Add screenshots of the **actual running application** in this section so visitors can see the interface and prediction output.

Suggested screenshots:

1. Main application / property input form.
2. Property valuation result showing the predicted price.
3. Interactive charts and comparable-property information.

Create a `screenshots/` directory in the repository and add your real screenshots. Then replace the example image paths below with the exact filenames you upload.

```markdown
![Property valuation input form](screenshots/property-input.png)
![Property valuation result](screenshots/valuation-result.png)
![Price visualisation](screenshots/price-visualisation.png)
```

> The image paths above are examples only. No application screenshots were included in the supplied setup instructions, so add the real screenshots before publishing.

## 🧰 Troubleshooting

### `streamlit` command not found

```bash
python -m pip install streamlit
```

### Module not found errors

Activate the project's virtual environment and install the dependencies:

```bash
pip install -r requirements.txt
```

Or install the packages listed in the setup notes:

```bash
pip install streamlit pandas numpy plotly scikit-learn matplotlib seaborn
```

### Port already in use

```bash
streamlit run app.py --server.port 8502
```

### Application does not open automatically

Open `http://localhost:8501` manually, or use the URL printed in the terminal. If you selected another port, use that port in your browser.

### Dependency installation problems

Upgrade pip and retry:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## 🚀 Future Improvements

Potential areas for further development:

- Document the dataset source, feature definitions, and preprocessing steps.
- Publish a reproducible evaluation report with R², RMSE, and MAE.
- Compare additional regression algorithms if they are part of the actual experiments.
- Add feature-importance or model-explainability visualisations.
- Improve location-specific valuation using updated property data.
- Add more examples and screenshots of prediction results.

## ⚠️ Disclaimer

This application provides machine-learning-based property price estimates for educational and informational purposes. It is not a certified property appraisal or financial recommendation. Actual market prices may differ due to location, market conditions, legal status, property condition, and other factors.

## 👨‍💻 Author

**Devansh Prajapati**

- GitHub: [@DevanshPrajapati28](https://github.com/DevanshPrajapati28)
- Project repository: [AI-Powered Real Estate Valuation](https://github.com/DevanshPrajapati28/AI-Powered-Real-Estate-Valuation)

---

If you find this project useful, consider giving the repository a ⭐ on GitHub.
