# 🐍 Python for Data Science — Beginner to Advanced

> A complete roadmap and reference guide to mastering Python for Data Science, from zero to expert level.

---

## 📌 Table of Contents

1. [About This Guide](#about-this-guide)
2. [Prerequisites](#prerequisites)
3. [Setup & Installation](#setup--installation)
4. [🟢 Beginner Level](#-beginner-level)
5. [🟡 Intermediate Level](#-intermediate-level)
6. [🔴 Advanced Level](#-advanced-level)
7. [Data Science Libraries](#data-science-libraries)
8. [Projects by Level](#projects-by-level)
9. [Learning Resources](#learning-resources)
10. [Contributing](#contributing)

---

## About This Guide

This guide covers everything you need to become a proficient Python Data Scientist — from basic syntax to machine learning, deep learning, and deploying models in production. Each section builds on the previous one.

---

## Prerequisites

- A computer with internet access
- Curiosity and patience 😊
- No prior programming experience needed for the beginner section

---

## Setup & Installation

### 1. Install Python
Download from [python.org](https://www.python.org/downloads/) (Python 3.9+ recommended)

```bash
python --version   # Verify installation
```

### 2. Install Anaconda (Recommended for Data Science)
Download from [anaconda.com](https://www.anaconda.com/) — comes with Jupyter, NumPy, Pandas, and more pre-installed.

### 3. Create a Virtual Environment
```bash
python -m venv ds_env
source ds_env/bin/activate        # macOS/Linux
ds_env\Scripts\activate           # Windows
```

### 4. Install Core Libraries
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter notebook
```

### 5. Launch Jupyter Notebook
```bash
jupyter notebook
```

---

## 🟢 Beginner Level

### 1. Python Basics

#### Variables & Data Types
```python
name = "Alice"          # str
age = 25                # int
gpa = 3.8               # float
is_student = True       # bool

print(type(name))       # <class 'str'>
```

#### Operators
```python
# Arithmetic
x = 10 + 5    # 15
x = 10 ** 2   # 100 (power)
x = 10 % 3    # 1   (modulo)

# Comparison
print(5 > 3)    # True
print(5 == 5)   # True
print(5 != 3)   # True
```

#### Strings
```python
text = "Hello, Data Science!"
print(text.upper())            # HELLO, DATA SCIENCE!
print(text.split(", "))        # ['Hello', 'Data Science!']
print(text[0:5])               # Hello
print(f"Length: {len(text)}")  # Length: 21
```

#### Lists
```python
scores = [85, 90, 78, 95, 88]
scores.append(100)
scores.sort()
print(scores[0])               # First element
print(scores[-1])              # Last element
print(scores[1:4])             # Slice
```

#### Dictionaries
```python
student = {
    "name": "Alice",
    "age": 25,
    "grades": [90, 85, 88]
}

print(student["name"])         # Alice
student["city"] = "Mumbai"     # Add new key
```

#### Tuples & Sets
```python
coordinates = (28.6, 77.2)     # Tuple — immutable
unique_items = {1, 2, 3, 3}   # Set — removes duplicates → {1, 2, 3}
```

---

### 2. Control Flow

#### If / Elif / Else
```python
score = 75

if score >= 90:
    print("A Grade")
elif score >= 75:
    print("B Grade")
else:
    print("C Grade")
```

#### Loops
```python
# For loop
for i in range(5):
    print(i)

# While loop
count = 0
while count < 5:
    print(count)
    count += 1

# List comprehension
squares = [x**2 for x in range(10)]
```

---

### 3. Functions
```python
def greet(name, greeting="Hello"):
    """Returns a greeting message."""
    return f"{greeting}, {name}!"

print(greet("Alice"))              # Hello, Alice!
print(greet("Bob", "Welcome"))     # Welcome, Bob!

# Lambda (anonymous function)
square = lambda x: x ** 2
print(square(5))                   # 25
```

---

### 4. File Handling
```python
# Write to file
with open("data.txt", "w") as f:
    f.write("Hello, Data Science!\n")

# Read from file
with open("data.txt", "r") as f:
    content = f.read()
    print(content)
```

---

### 5. Error Handling
```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Error: {e}")
except Exception as e:
    print(f"Unexpected error: {e}")
finally:
    print("Execution complete")
```

---

## 🟡 Intermediate Level

### 1. Object-Oriented Programming (OOP)
```python
class DataScientist:
    company = "Tech Corp"   # Class attribute

    def __init__(self, name, skills):
        self.name = name
        self.skills = skills

    def introduce(self):
        return f"I'm {self.name}, skilled in {', '.join(self.skills)}"

    def add_skill(self, skill):
        self.skills.append(skill)


# Inheritance
class SeniorDataScientist(DataScientist):
    def __init__(self, name, skills, years_exp):
        super().__init__(name, skills)
        self.years_exp = years_exp

    def introduce(self):
        base = super().introduce()
        return f"{base} with {self.years_exp} years of experience"


ds = SeniorDataScientist("Alice", ["Python", "ML"], 5)
print(ds.introduce())
```

---

### 2. NumPy — Numerical Computing
```python
import numpy as np

# Arrays
arr = np.array([1, 2, 3, 4, 5])
matrix = np.zeros((3, 3))
identity = np.eye(3)

# Array operations (vectorized — much faster than loops)
arr2 = np.array([10, 20, 30, 40, 50])
print(arr + arr2)           # Element-wise addition
print(arr * 2)              # Scalar multiplication
print(np.dot(arr, arr2))    # Dot product

# Statistics
data = np.random.randn(1000)
print(f"Mean: {np.mean(data):.4f}")
print(f"Std:  {np.std(data):.4f}")
print(f"Min:  {np.min(data):.4f}")

# Reshaping
arr_2d = arr.reshape(5, 1)
arr_flat = arr_2d.flatten()

# Boolean indexing
mask = arr > 3
print(arr[mask])            # [4, 5]
```

---

### 3. Pandas — Data Manipulation
```python
import pandas as pd

# Create DataFrame
df = pd.DataFrame({
    "Name": ["Alice", "Bob", "Charlie", "Diana"],
    "Age": [25, 30, 35, 28],
    "Salary": [60000, 75000, 90000, 65000],
    "Department": ["Data", "ML", "Data", "ML"]
})

# Exploration
print(df.head())
print(df.info())
print(df.describe())

# Selection
print(df["Name"])                          # Single column
print(df[["Name", "Salary"]])             # Multiple columns
print(df.loc[0])                           # Row by label
print(df.iloc[0:2])                        # Row by index

# Filtering
high_earners = df[df["Salary"] > 70000]
data_team = df[df["Department"] == "Data"]

# Aggregation
print(df.groupby("Department")["Salary"].mean())

# Handling Missing Values
df_with_na = df.copy()
df_with_na.loc[0, "Salary"] = None
df_cleaned = df_with_na.dropna()
df_filled = df_with_na.fillna(df_with_na["Salary"].mean())

# Merge DataFrames
dept_df = pd.DataFrame({
    "Department": ["Data", "ML"],
    "Budget": [500000, 700000]
})
merged = pd.merge(df, dept_df, on="Department")

# Read/Write CSV
df.to_csv("employees.csv", index=False)
df_loaded = pd.read_csv("employees.csv")
```

---

### 4. Data Visualization

#### Matplotlib
```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.figure(figsize=(10, 4))
plt.plot(x, y, color="blue", linewidth=2, label="sin(x)")
plt.title("Sine Wave")
plt.xlabel("x")
plt.ylabel("y")
plt.legend()
plt.grid(True)
plt.savefig("sine_wave.png", dpi=150)
plt.show()
```

#### Seaborn (Statistical Plots)
```python
import seaborn as sns
import pandas as pd

# Load sample dataset
tips = sns.load_dataset("tips")

# Distribution plot
sns.histplot(tips["total_bill"], bins=30, kde=True)

# Scatter plot
sns.scatterplot(data=tips, x="total_bill", y="tip", hue="sex", size="size")

# Correlation heatmap
corr = tips.select_dtypes(include="number").corr()
sns.heatmap(corr, annot=True, cmap="coolwarm", fmt=".2f")

plt.show()
```

---

### 5. Exploratory Data Analysis (EDA)
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

def eda_summary(df):
    print("=" * 50)
    print("DATASET OVERVIEW")
    print("=" * 50)
    print(f"Shape: {df.shape}")
    print(f"\nColumn Types:\n{df.dtypes}")
    print(f"\nMissing Values:\n{df.isnull().sum()}")
    print(f"\nDuplicate Rows: {df.duplicated().sum()}")
    print(f"\nBasic Statistics:\n{df.describe()}")
    
    # Plot distributions for numerical columns
    numeric_cols = df.select_dtypes(include="number").columns
    df[numeric_cols].hist(figsize=(12, 8), bins=20)
    plt.suptitle("Feature Distributions")
    plt.tight_layout()
    plt.show()

df = pd.read_csv("your_dataset.csv")
eda_summary(df)
```

---

## 🔴 Advanced Level

### 1. Machine Learning with Scikit-Learn

#### Complete ML Pipeline
```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split, cross_val_score, GridSearchCV
from sklearn.preprocessing import StandardScaler, LabelEncoder
from sklearn.pipeline import Pipeline
from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report, confusion_matrix, roc_auc_score
import matplotlib.pyplot as plt
import seaborn as sns

# 1. Load and prepare data
from sklearn.datasets import load_breast_cancer
data = load_breast_cancer()
X = pd.DataFrame(data.data, columns=data.feature_names)
y = pd.Series(data.target)

# 2. Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)

# 3. Build Pipeline
pipeline = Pipeline([
    ("scaler", StandardScaler()),
    ("model", RandomForestClassifier(random_state=42))
])

# 4. Hyperparameter Tuning
param_grid = {
    "model__n_estimators": [100, 200],
    "model__max_depth": [None, 10, 20],
    "model__min_samples_split": [2, 5]
}

grid_search = GridSearchCV(pipeline, param_grid, cv=5, scoring="roc_auc", n_jobs=-1)
grid_search.fit(X_train, y_train)

best_model = grid_search.best_estimator_
print(f"Best Params: {grid_search.best_params_}")

# 5. Evaluate
y_pred = best_model.predict(X_test)
y_proba = best_model.predict_proba(X_test)[:, 1]

print("\nClassification Report:")
print(classification_report(y_test, y_pred))
print(f"ROC-AUC Score: {roc_auc_score(y_test, y_proba):.4f}")

# 6. Feature Importance
importances = best_model.named_steps["model"].feature_importances_
feat_importance = pd.Series(importances, index=X.columns).sort_values(ascending=False)

plt.figure(figsize=(10, 6))
feat_importance.head(15).plot(kind="bar")
plt.title("Top 15 Feature Importances")
plt.tight_layout()
plt.show()
```

---

### 2. Deep Learning with TensorFlow / Keras
```python
import tensorflow as tf
from tensorflow.keras import layers, models, callbacks
from tensorflow.keras.optimizers import Adam
import numpy as np

# Build Neural Network
def build_model(input_dim, num_classes):
    model = models.Sequential([
        layers.Input(shape=(input_dim,)),
        layers.Dense(256, activation="relu"),
        layers.BatchNormalization(),
        layers.Dropout(0.3),
        layers.Dense(128, activation="relu"),
        layers.BatchNormalization(),
        layers.Dropout(0.2),
        layers.Dense(64, activation="relu"),
        layers.Dense(num_classes, activation="softmax")
    ])
    return model

model = build_model(input_dim=30, num_classes=2)
model.compile(
    optimizer=Adam(learning_rate=0.001),
    loss="sparse_categorical_crossentropy",
    metrics=["accuracy"]
)
model.summary()

# Callbacks
early_stop = callbacks.EarlyStopping(patience=10, restore_best_weights=True)
lr_scheduler = callbacks.ReduceLROnPlateau(factor=0.5, patience=5)

# Train
history = model.fit(
    X_train, y_train,
    epochs=100,
    batch_size=32,
    validation_split=0.2,
    callbacks=[early_stop, lr_scheduler],
    verbose=1
)
```

---

### 3. Natural Language Processing (NLP)
```python
import nltk
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.naive_bayes import MultinomialNB
from sklearn.pipeline import Pipeline

# Text preprocessing
import re
def clean_text(text):
    text = text.lower()
    text = re.sub(r"[^a-z\s]", "", text)
    text = re.sub(r"\s+", " ", text).strip()
    return text

# TF-IDF + Naive Bayes pipeline
texts = ["I love data science", "Python is amazing", "Machine learning rocks"]
labels = [1, 1, 1]

nlp_pipeline = Pipeline([
    ("tfidf", TfidfVectorizer(max_features=5000, ngram_range=(1, 2))),
    ("clf", MultinomialNB())
])

# Transformers (Modern NLP)
from transformers import pipeline
sentiment = pipeline("sentiment-analysis")
result = sentiment("Python is an amazing language for Data Science!")
print(result)   # [{'label': 'POSITIVE', 'score': 0.99}]
```

---

### 4. Time Series Analysis
```python
import pandas as pd
import numpy as np
from statsmodels.tsa.arima.model import ARIMA
from statsmodels.tsa.seasonal import seasonal_decompose
import matplotlib.pyplot as plt

# Load time series
dates = pd.date_range("2020-01-01", periods=365, freq="D")
values = np.cumsum(np.random.randn(365)) + 100
ts = pd.Series(values, index=dates)

# Decompose
decomposition = seasonal_decompose(ts, model="additive", period=30)
decomposition.plot()
plt.show()

# ARIMA model
model = ARIMA(ts, order=(5, 1, 2))
result = model.fit()
forecast = result.forecast(steps=30)
print(forecast)
```

---

### 5. Model Deployment with Flask
```python
# app.py
from flask import Flask, request, jsonify
import pickle
import numpy as np

app = Flask(__name__)

# Load pre-trained model
with open("model.pkl", "rb") as f:
    model = pickle.load(f)

@app.route("/predict", methods=["POST"])
def predict():
    data = request.get_json()
    features = np.array(data["features"]).reshape(1, -1)
    prediction = model.predict(features)
    probability = model.predict_proba(features).max()
    
    return jsonify({
        "prediction": int(prediction[0]),
        "confidence": round(float(probability), 4)
    })

if __name__ == "__main__":
    app.run(debug=True, port=5000)
```

---

## Data Science Libraries

| Library | Purpose | Level |
|---|---|---|
| `numpy` | Numerical computing, arrays | Beginner |
| `pandas` | Data manipulation & analysis | Beginner |
| `matplotlib` | Plotting & visualization | Beginner |
| `seaborn` | Statistical visualization | Intermediate |
| `scikit-learn` | Machine learning | Intermediate |
| `scipy` | Scientific computing | Intermediate |
| `statsmodels` | Statistical modeling | Intermediate |
| `tensorflow` / `keras` | Deep learning | Advanced |
| `pytorch` | Deep learning (research) | Advanced |
| `xgboost` / `lightgbm` | Gradient boosting | Advanced |
| `nltk` / `spacy` | Natural language processing | Advanced |
| `transformers` | State-of-the-art NLP models | Advanced |
| `plotly` | Interactive visualizations | Intermediate |
| `streamlit` | ML app deployment | Advanced |
| `mlflow` | ML experiment tracking | Advanced |

---

## Projects by Level

### 🟢 Beginner Projects
- **Sales Data Analysis** — Load a CSV, clean data, compute summary statistics
- **Weather Data Visualizer** — Plot temperature trends using Matplotlib
- **Student Grade Calculator** — Use functions, loops, and conditionals

### 🟡 Intermediate Projects
- **Titanic Survival Prediction** — Classification with Scikit-Learn
- **House Price Prediction** — Regression analysis with feature engineering
- **Customer Segmentation** — K-Means clustering
- **Sentiment Analysis** — Analyze product reviews with NLP

### 🔴 Advanced Projects
- **Real-Time Stock Market Dashboard** — Streamlit + Pandas + Plotly
- **Image Classification CNN** — TensorFlow/Keras on CIFAR-10
- **Recommendation System** — Collaborative filtering
- **End-to-End ML Pipeline** — Data ingestion → training → deployment → monitoring
- **Chatbot with Transformers** — Fine-tune a pre-trained LLM

---

## Learning Resources

### Documentation
- [Python Official Docs](https://docs.python.org/3/)
- [NumPy Docs](https://numpy.org/doc/)
- [Pandas Docs](https://pandas.pydata.org/docs/)
- [Scikit-Learn Docs](https://scikit-learn.org/stable/)
- [TensorFlow Docs](https://www.tensorflow.org/api_docs)

### Courses
- [Kaggle Learn — Free Micro-Courses](https://www.kaggle.com/learn)
- [fast.ai — Practical Deep Learning](https://www.fast.ai/)
- [CS229: Machine Learning — Stanford](https://cs229.stanford.edu/)

### Books
- *Python for Data Analysis* — Wes McKinney
- *Hands-On Machine Learning* — Aurélien Géron
- *Deep Learning* — Goodfellow, Bengio, Courville

### Practice Platforms
- [Kaggle](https://www.kaggle.com/) — Datasets & competitions
- [LeetCode](https://leetcode.com/) — Python coding practice
- [Google Colab](https://colab.research.google.com/) — Free GPU/TPU notebooks

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/new-topic`
3. Commit your changes: `git commit -m "Add: New topic section"`
4. Push to the branch: `git push origin feature/new-topic`
5. Open a Pull Request

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ for the Data Science Community**

⭐ Star this repo if you find it helpful!

</div>
