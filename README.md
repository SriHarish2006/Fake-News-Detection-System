# 📰 Fake News Detection System

<p align="center">

### 🤖 AI-Powered News Classification Using NLP & Machine Learning

🤖 Machine Learning-Based Fake News Classification

An intelligent Fake News Detection System that uses Natural Language Processing (NLP) and Machine Learning to classify news articles as Real or Fake.

The system converts news text into numerical features using TF-IDF (Term Frequency–Inverse Document Frequency) and applies machine learning classification algorithms to identify potentially misleading or fabricated news content.
</p>

---

## 📌 About The Project

The **Fake News Detection System** is a Machine Learning and Natural Language Processing project designed to classify news content as **Fake** or **Real** based on textual patterns.

The system processes the submitted news text, cleans and transforms the content using NLP techniques, converts the text into numerical features using **TF-IDF**, and passes the resulting features to a trained Machine Learning classification model.

A **Streamlit web application** provides a simple and interactive interface where users can enter news content and receive a prediction.

> ⚠️ **Important:** This system provides a machine-learning classification prediction. It should not be treated as definitive proof that a news article is factually true or false. Important claims should be independently verified using reliable sources.

---

# 🎯 Project Objectives

The main objectives of this project are:

* 📰 Automatically classify news as **Fake or Real**
* 🧠 Apply **Natural Language Processing**
* 🔤 Convert text into numerical features using **TF-IDF**
* 🤖 Train Machine Learning classification models
* 📊 Evaluate model performance using classification metrics
* 🌐 Build an interactive **Streamlit web application**
* ⚡ Provide fast predictions from user-provided news content
* 🎓 Demonstrate a practical application of Machine Learning and NLP

---

# ✨ Key Features

| Feature                | Description                                     |
| ---------------------- | ----------------------------------------------- |
| 📰 News Classification | Predicts whether submitted news is Fake or Real |
| 🧠 NLP Processing      | Cleans and prepares textual data                |
| 🔤 TF-IDF              | Converts news text into numerical features      |
| 🤖 Machine Learning    | Uses classification algorithms for prediction   |
| 🌐 Streamlit UI        | Interactive browser-based application           |
| ⚡ Fast Prediction      | Generates predictions quickly                   |
| 📊 Model Evaluation    | Supports standard classification metrics        |
| 🔄 Reusable Model      | Trained model can be saved and reused           |
| 💻 Beginner Friendly   | Simple project structure and workflow           |

---

# 🏗️ System Architecture

```text
                         ┌─────────────────────┐
                         │        USER         │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │   STREAMLIT WEB UI  │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │    NEWS ARTICLE     │
                         │       INPUT         │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │  TEXT PREPROCESSING │
                         │                     │
                         │ • Lowercase         │
                         │ • Cleaning          │
                         │ • Normalization     │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │  TF-IDF VECTORIZER  │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │  ML CLASSIFICATION  │
                         │        MODEL        │
                         └──────────┬──────────┘
                                    │
                         ┌──────────┴──────────┐
                         ▼                     ▼
                  ┌─────────────┐       ┌─────────────┐
                  │  ✅ REAL    │       │  ⚠️ FAKE    │
                  │    NEWS     │       │    NEWS     │
                  └─────────────┘       └─────────────┘
```

---

# 🔄 Machine Learning Workflow

```text
                 ┌──────────────────┐
                 │      Dataset     │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Data Cleaning    │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Text Processing  │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ TF-IDF           │
                 │ Vectorization    │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Train / Test     │
                 │ Split            │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Model Training   │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Model Evaluation │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Save Model       │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Streamlit App    │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Fake / Real      │
                 │ Prediction       │
                 └──────────────────┘
```

---

# 🧠 How It Works

## 1. 🗂️ Dataset

The system uses a labeled news dataset containing examples of fake and real news.

The data generally contains textual information such as:

* News title
* News article text
* Label

The label represents the target classification.

```text
0 → Fake News
1 → Real News
```

The exact label encoding depends on the dataset used during training.

---

## 2. 🧹 Text Preprocessing

Before Machine Learning, the text is cleaned and prepared.

Typical preprocessing operations include:

* Converting text to lowercase
* Removing unnecessary characters
* Removing unwanted spaces
* Cleaning textual noise
* Preparing text for vectorization

Example:

```text
Original:
"BREAKING!!! Amazing NEWS!!! Visit www.example.com"

After Cleaning:
"breaking amazing news visit"
```

---

# 🔤 TF-IDF Feature Extraction

The system uses **TF-IDF — Term Frequency-Inverse Document Frequency** to transform news text into numerical features.

TF-IDF gives importance to words based on:

* How frequently a word occurs in a document
* How rare or common the word is across the complete dataset

Conceptually:

```text
News Text
    ↓
Text Cleaning
    ↓
Tokenized Words
    ↓
TF-IDF Vectorization
    ↓
Numerical Feature Vector
    ↓
Machine Learning Model
```

---

# 🤖 Machine Learning

The transformed TF-IDF features are provided to a classification model.

The project is designed around traditional Machine Learning classification techniques suitable for text classification.

Potential models include:

### Logistic Regression

A supervised learning algorithm commonly used for binary classification.

```text
TF-IDF Features
       ↓
Logistic Regression
       ↓
Probability
       ↓
Fake / Real
```

### Random Forest

An ensemble learning algorithm that combines multiple decision trees to make predictions.

```text
TF-IDF Features
       ↓
Multiple Decision Trees
       ↓
Voting / Aggregation
       ↓
Fake / Real
```

The final model used by the application should match the model actually trained and saved in the project.

---

# 🛠️ Technology Stack

| Technology         | Purpose               |
| ------------------ | --------------------- |
| 🐍 Python          | Core Programming      |
| 🧠 Scikit-learn    | Machine Learning      |
| 📝 NLP             | Text Processing       |
| 🔤 TF-IDF          | Feature Extraction    |
| 🐼 Pandas          | Dataset Processing    |
| 🔢 NumPy           | Numerical Computation |
| 📊 Matplotlib      | Visualization         |
| 📈 Seaborn         | Data Visualization    |
| 🌐 Streamlit       | Web Application       |
| 💾 Joblib / Pickle | Model Serialization   |
| 💻 VS Code         | Development           |
| 🔧 Git             | Version Control       |
| 🐙 GitHub          | Project Hosting       |

---

# 📁 Project Structure

```text
Fake-News-Detection/
│
├── app.py
├── README.md
├── requirements.txt
│
├── data/
│   └── dataset.csv
│
├── model/
│   ├── model.pkl
│   └── vectorizer.pkl
│
├── notebooks/
│   └── fake_news_detection.ipynb
│
└── assets/
    ├── home.png
    ├── real-news.png
    └── fake-news.png
```

> Keep only the folders/files that actually exist in your repository. Rename `dataset.csv`, model files, and notebook names if your project uses different filenames.

---

# 💻 Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/SriHarish2006/Fake-News-Detection.git
```

## 2️⃣ Open the Project

```bash
cd Fake-News-Detection
```

## 3️⃣ Create Virtual Environment

### Windows

```bash
python -m venv venv
```

Activate:

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
```

Activate:

```bash
source venv/bin/activate
```

---

# 📦 Install Dependencies

Run:

```bash
python -m pip install -r requirements.txt
```

Example `requirements.txt`:

```text
pandas
numpy
scikit-learn
matplotlib
seaborn
streamlit
joblib
nltk
```

---

# ▶️ Run the Application

Start the Streamlit application using:

```bash
streamlit run app.py
```

If your Windows Python environment has launcher/path issues, use:

```bash
python -m streamlit run app.py
```

The application will normally be available at:

```text
http://localhost:8501
```

---

# 🖥️ Application

The Streamlit application allows users to enter news content and obtain a classification result.

### Example Input

```text
Scientists have announced a new research discovery after
conducting a large-scale study involving thousands of participants.
```

### Example Output

```text
┌─────────────────────────────────┐
│       🔎 PREDICTION RESULT      │
├─────────────────────────────────┤
│                                 │
│          ✅ REAL NEWS            │
│                                 │
│   Model classification result   │
│                                 │
└─────────────────────────────────┘
```

Another possible prediction:

```text
┌─────────────────────────────────┐
│       🔎 PREDICTION RESULT      │
├─────────────────────────────────┤
│                                 │
│          ⚠️ FAKE NEWS           │
│                                 │
│   Model classification result   │
│                                 │
└─────────────────────────────────┘
```

> These are interface examples only. Actual predictions depend on the trained model and input text.

---

# 📸 Screenshots

Create an `assets` folder and place your screenshots there.

### 🏠 Application Home Page

```text
![Home Page](assets/home.png)
```

### 📰 News Input

```text
![News Input](assets/news-input.png)
```

### ✅ Real News Prediction

```text
![Real News Prediction](assets/real-news.png)
```

### ⚠️ Fake News Prediction

```text
![Fake News Prediction](assets/fake-news.png)
```

---

# 📊 Model Evaluation

The model should be evaluated using multiple classification metrics rather than accuracy alone.

### Evaluation Metrics

| Metric           | Meaning                                                  |
| ---------------- | -------------------------------------------------------- |
| Accuracy         | Percentage of correctly classified samples               |
| Precision        | How many predicted positive cases were actually positive |
| Recall           | How many actual positive cases were correctly detected   |
| F1-Score         | Balance between Precision and Recall                     |
| Confusion Matrix | Displays correct and incorrect predictions               |

### Model Comparison

| Model               |         Accuracy |        Precision |           Recall |         F1-Score |
| ------------------- | ---------------: | ---------------: | ---------------: | ---------------: |
| Logistic Regression | Add actual value | Add actual value | Add actual value | Add actual value |
| Random Forest       | Add actual value | Add actual value | Add actual value | Add actual value |

### Example Format

```text
Model Performance

Logistic Regression
Accuracy  : XX.XX%
Precision : XX.XX%
Recall    : XX.XX%
F1-Score  : XX.XX%

Random Forest
Accuracy  : XX.XX%
Precision : XX.XX%
Recall    : XX.XX%
F1-Score  : XX.XX%
```

> **Important:** Replace the values with the actual output from your training/evaluation code. Do not claim an accuracy simply because it is commonly reported by similar projects.

---

# 📈 Confusion Matrix

A confusion matrix helps understand how the classifier performs on both classes.

```text
                         Predicted
                     Fake        Real
                 ┌──────────┬──────────┐
Actual   Fake    │    TN    │    FP    │
                 ├──────────┼──────────┤
         Real    │    FN    │    TP    │
                 └──────────┴──────────┘
```

Where:

* **TP** → Correctly predicted Real
* **TN** → Correctly predicted Fake
* **FP** → Fake predicted as Real
* **FN** → Real predicted as Fake

The exact interpretation depends on how the target labels are encoded in the implementation.

---

# 🎯 Project Goals

### Technical Goals

* Implement NLP preprocessing
* Apply TF-IDF vectorization
* Train supervised classification models
* Evaluate classification performance
* Build a reusable prediction pipeline
* Develop a Streamlit interface

### Practical Goals

* Provide a simple news-classification tool
* Demonstrate NLP in a real-world problem
* Help users identify content that may require further verification
* Create an end-to-end Machine Learning project

---

# 🌍 Real-World Applications

The underlying approach can be explored for:

### 📰 Digital Media

Automated screening of large amounts of news content.

### 📱 Social Media

Identifying content that may require additional review.

### 🔎 Content Moderation

Supporting moderation workflows.

### 🎓 Education

Demonstrating NLP and Machine Learning concepts.

### 🏢 Information Systems

Helping organizations prioritize content for human verification.

> The system should be considered a screening/classification tool rather than an independent fact-checking authority.

---

# ⚡ Advantages

* ✅ Automated classification
* ✅ NLP-based text analysis
* ✅ TF-IDF feature extraction
* ✅ Fast predictions
* ✅ Interactive Streamlit interface
* ✅ Easy to understand workflow
* ✅ Reusable trained model
* ✅ Suitable for academic demonstration
* ✅ Can be extended with advanced NLP models

---

# ⚠️ Limitations

* Dataset quality affects model performance.
* Machine Learning models can learn biases present in training data.
* New misinformation patterns may not be recognized well.
* Satire and opinion-based content can be difficult to classify.
* Text-only classification does not independently verify factual claims.
* Predictions may include false positives and false negatives.
* Real-world deployment would require continuous monitoring and model updates.

---

# 🔮 Future Enhancements

The project can be extended with:

### 🤖 Advanced AI

* BERT
* RoBERTa
* DistilBERT
* Transformer-based NLP
* Deep Learning models

### 🔎 Explainable AI

* SHAP
* LIME
* Keyword-level explanations
* Prediction confidence visualization

### 🌐 Web Features

* URL-based news analysis
* News article extraction
* Browser extension
* Real-time news verification

### 📰 External Verification

* Integration with trusted fact-checking sources
* Evidence retrieval
* Source credibility analysis
* Cross-source comparison

### 🌍 Multilingual Support

Support for:

```text
English
Tamil
Hindi
Telugu
Malayalam
Kannada
```

### ☁️ Deployment

* Streamlit Community Cloud
* Docker
* AWS
* Azure
* Google Cloud

---

# 🔐 Responsible AI

This project is intended primarily for **educational and research purposes**.

A Machine Learning model can identify patterns associated with its training data, but it cannot independently establish the truth of every real-world claim.

Users should verify important information using:

* Reliable news organizations
* Official government sources
* Primary documents
* Established fact-checking organizations
* Multiple independent sources

---

# 📚 Learning Outcomes

Through this project, the following concepts are demonstrated:

```text
Python
   ↓
Data Processing
   ↓
Natural Language Processing
   ↓
TF-IDF
   ↓
Machine Learning
   ↓
Model Evaluation
   ↓
Streamlit
   ↓
Git & GitHub
```

The project provides practical experience in building an end-to-end **NLP + Machine Learning + Web Application** pipeline.

---

# 👨‍💻 Author

## Sri Harish

**B.E. Computer Science and Engineering**

### Areas of Interest

* 🤖 Artificial Intelligence
* 🧠 Machine Learning
* 📊 Data Analytics
* 📈 Business Intelligence
* 🐍 Python
* 🗄️ SQL
* 💻 Software Development

---

# ⭐ Support the Project

If you find this project useful:

⭐ **Star the repository**

🍴 **Fork the repository**

🐛 **Report issues**

💡 **Suggest improvements**

🤝 **Contribute to the project**

---

# 📄 License

This project is developed for **educational and academic purposes**.

If you intend to distribute or modify the project publicly, add an appropriate open-source license such as **MIT License**.

---

# 🏷️ Topics

```text
fake-news-detection
machine-learning
natural-language-processing
nlp
python
scikit-learn
tf-idf
text-classification
streamlit
artificial-intelligence
data-science
fake-news-classification
machine-learning-project
python-project
college-project
```

---

<p align="center">

### 📰 Fake News Detection System

**Built with Python • NLP • Machine Learning • TF-IDF • Streamlit**

⭐ Star the repository if you found it useful!

</p>
