# AURA.AI: Student Academic Performance Forecasting Suite

AURA.AI is a premium, end-to-end Machine Learning web application that forecasts student mathematical competency scores. Driven by a high-precision multi-model ensemble pipeline (including CatBoost, XGBoost, and Random Forest), the suite processes key socio-demographic and historic test parameters to generate instant inferences.

The frontend features a state-of-the-art **glassmorphic dark-mode dashboard** built using custom CSS tokens and Bootstrap 5, giving it the look and feel of an enterprise-grade AI prediction platform.

---

## 🌟 Key Features

* **Multi-Model Regression Ensemble**: Trains and evaluates multiple regressors (Random Forest, Decision Tree, Gradient Boosting, XGBoost, CatBoost, AdaBoost, Linear Regression) using `GridSearchCV` hyperparameter tuning to select the optimal model.
* **Automated Transformation Pipeline**: Employs a robust preprocessing setup featuring `SimpleImputer` for handling missing data, `StandardScaler` for numeric scaling, and `OneHotEncoder` for categoricals.
* **Modern Glassmorphic Dashboard**: A fully responsive web interface featuring subtle breathing neon animations, custom outline glow on focus states, and a dynamic prediction visualization center.
* **Intelligent Score Benchmarking**: Active states provide dynamic graphical scales and color-coded alert advice based on predicted score brackets.
* **Production-Ready & Robust**: Full input validation guards against empty submissions, preventing server-side runtime crashes.

---

## 📂 Project Structure

```bash
├── artifacts/               # Packaged splits and pickled preprocessing/model assets
├── catboost_info/           # CatBoost execution logs
├── notebook/                # Jupyter Notebooks containing EDA and prototyping
│   ├── data/
│   │   └── stud.csv         # Original raw dataset
│   ├── 1. EDA STUDENT PERFORMANCE.ipynb
│   └── 2. MODEL TRAINING.ipynb
├── src/                     # Core application source package
│   ├── components/          # Pipeline component layers
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── pipeline/            # Operational pipelines
│   │   ├── train_pipeline.py
│   │   └── predict_pipeline.py
│   ├── exception.py         # Custom traceback exception handling
│   ├── logger.py            # Automated logging utility
│   └── utils.py             # Global utility helpers
├── static/                  # Static assets
│   └── css/
│       └── style.css        # Premium custom CSS variables & animations
├── templates/               # Flask HTML templates
│   ├── home.html            # Main interactive analytics dashboard
│   └── index.html           # High-tech portal welcome page
├── app.py                   # Main Flask controller app
├── requirements.txt         # Package dependencies
└── setup.py                 # Setuptools package configuration
```

---

## 🛠️ Technology Stack

| Layer | Technologies |
| :--- | :--- |
| **Backend & ML** | Python 3, Flask, scikit-learn, CatBoost, XGBoost, Pandas, NumPy, Dill |
| **Frontend & UI** | HTML5, Vanilla CSS3 (Custom Variables & Keyframes), Bootstrap 5, Bootstrap Icons |
| **Packaging & CI** | Setuptools, Git |

---

## 🚀 Getting Started

Follow these steps to set up and run AURA.AI locally.

### Prerequisites
* Python 3.8 or higher installed on your system.

### 1. Clone & Set Up Directory
```bash
git clone https://github.com/ankit-bind/MLProject_Student_Dataset.git
cd MLProject_Student_Dataset
```

### 2. Configure Virtual Environment & Install Dependencies
```bash
# Create virtual environment
python -m venv venv

# Activate on Windows
.\venv\Scripts\activate

# Activate on Linux/macOS
source venv/bin/activate

# Install required packages
pip install -r requirements.txt
```

### 3. Run Ingestion and Training Pipelines
Generate the model splits, transform the variables, and train/tune the ensemble models to produce the artifacts:
```bash
python src/components/data_ingestion.py
```
This script automatically executes data ingestion, transformation, and model training, saving `model.pkl` and `preprocessor.pkl` to the `artifacts/` folder.

### 4. Launch the Web Application
```bash
python app.py
```

### 5. Access the Platform
Open your browser and navigate to:
```bash
http://127.0.0.1:5000/
```

---

## 🛡️ License & Attribution
* Designed, developed, and deployed by **Ankit** (itz.ankitbind01@gmail.com).
* Built as a comprehensive end-to-end machine learning study and integration case.