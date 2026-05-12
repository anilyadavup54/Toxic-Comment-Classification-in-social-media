# Toxic Comment Classification in Social Media

This project automatically detects and classifies toxic comments in social‑media style text using **Natural Language Processing (NLP)** and **multi‑label text classification**. The model flags comments that are toxic, obscene, threatening, insulting, or contain identity‑based hate, helping platforms moderate harmful content. [web:4][web:9]

---

## 📌 Problem Statement
Online discussions often contain harmful comments that discourage participation and create a negative environment. This project aims to:
- Identify toxic behavior in user comments.
- Classify each comment into one or more of the following categories:
  - `toxic`
  - `severe_toxic`  
  - `obscene`
  - `threat`
  - `insult`
  - `identity_hate`  

---

## 📦 Dataset
The project is based on the **Jigsaw Toxic Comment Classification Challenge** dataset (Wikipedia comments labeled by human raters). [web:4][web:7]  
- Training set: ~159k comments with six binary toxicity labels.
- File structure (typical):
  - `data/train.csv` – labeled training data.
  - `data/test.csv` – unlabeled test data (for predictions).
  - `data/test_labels.csv` – optional, for evaluation.

---

## 🧠 Model & Approach
- **Task type**: Multi‑label text classification (a comment can belong to multiple toxicity classes). [web:4][web:8]  
- **Preprocessing**:
  - Text cleaning: lowercase, remove HTML, special characters, URLs.
  - Tokenization and sequence padding for deep‑learning models.
  - Vectorization via TF‑IDF or embeddings (e.g., Word2Vec / GloVe / BERT‑style tokens).
- **Model(s)** (adjust based on your code):
  - Option A: Classical ML (e.g., Logistic Regression or SVM with TF‑IDF). [web:9][web:10]  
  - Option B: Deep learning (e.g., LSTM / BiLSTM / CNN‑based neural network). [web:11][web:15]  
  - Option C: Transformer‑based (e.g., BERT / DistilBERT fine‑tuned on toxic‑comment data). [web:4][web:15]  

*(You can replace this section with your actual model, e.g., “BERT‑based model trained on 159k comments” or “LSTM‑CNN hybrid classifier”.)*

---

## 📊 Performance (Placeholder)
Typical toxicity‑classification projects achieve metrics such as: [web:4][web:9]  
- Macro‑ / micro‑AUC in the **0.90–0.95 range** across all six labels.
- Binary classification metrics (precision, recall, F1) per class.

Update this section with your actual:
- `AUC‑ROC scores`,
- `F1‑score per class`,
- `overall accuracy` or `precision‑recall` values.

---

## 🛠️ Installation & Usage

### 1. Clone the repo
```bash
git clone https://github.com/anilyadavup54/Toxic-Comment-Classification-in-social-media.git
cd Toxic-Comment-Classification-in-social-media
```

### 2. Create virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate     # Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

*(If your repo does not have `requirements.txt`, create it with `pip freeze > requirements.txt` or add your main packages manually, e.g., `numpy`, `pandas`, `scikit‑learn`, `torch` / `tensorflow`, `transformers`, `flask`).* [web:10]

### 4. Train the model
```bash
python train.py
```
or
```bash
python src/train.py
```
*(Adjust path to your actual training script.)*

### 5. Run the inference / demo
If you have a **Flask** or **Gradio** web app:

**Flask example**:
```bash
python app.py
```
Then open `http://localhost:5000` and type a comment to see toxicity predictions.

**Gradio example**:
```bash
python app.py
```
Then open `http://localhost:7860` for a simple UI.

*(Adapt the command and port to match your deployment script.)* [web:1][web:10]

---

#"It's on the local system because of the file size."
Toxic-Comment-Classification-in-social-media/
├── data/
│ ├── train.csv
│ ├── test.csv
│ └── test_labels.csv
├── models/
│ └── best_model.pkl / bert_model/
├── notebooks/
│ └── exploratory_data_analysis.ipynb
├── src/
│ ├── data_preprocessing.py
│ ├── modeling.py
│ └── evaluation.py
├── app.py # or webapp/app.py
├── train.py
├── inference.py
├── requirements.txt
└── README.md



---

## 🚀 Future Work
- Add **multi‑lingual support** (e.g., Hindi + English mix common in Indian social media).  
- Integrate with real‑time APIs for Telegram, Discord, or YouTube‑style comment moderation. [web:15]  
- Deploy model as a **REST API** (FastAPI / Flask) for production use.

---

## 📜 License
This project is open‑source. You can choose a license (e.g., `MIT`) and add it to your repo if you haven’t already.  
If unsure, MIT is a common choice for demo‑style ML projects. [web:5][web:9]



## 📂 Repository Structure (Example)
Adjust paths to match your actual folder layout:
