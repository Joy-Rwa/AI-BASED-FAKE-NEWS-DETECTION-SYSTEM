# FraudGuard AI — Fraud Detection for Facebook Marketplace

An NLP and BERT-driven analysis console that classifies Facebook Marketplace
business posts as **genuine** or **fraudulent**, with transparent, explainable
scoring built for analysts and moderators.

This repository contains the research prototype and supporting documents for a
final-year dissertation on detecting fraudulent business information on Facebook
Marketplace, with a focus on the Rwandan and East African context.

---

## ✨ Features

- **AI Detection** — analyses a post and returns a Genuine/Fraudulent verdict,
  confidence score, risk level, and highlighted suspicious tokens.
- **Sign in & Create account** — full authentication flow; new accounts are saved
  in the browser (via `localStorage`) so you can sign in again. Demo roles included.
- **Dashboard & Analytics** — KPIs, fraud trends, and charts.
- **Model comparison** — Logistic Regression, Naïve Bayes, and a fine-tuned BERT
  model (BERT ≈ **94.8%** accuracy, **0.948** F1 on the test set).
- **Marketplace posts, Sellers registry, NLP pipeline, Reports, User management,
  Settings, Help.**
- **No backend, no build step, no external dependencies** — the whole app is a
  single HTML file that runs in any modern browser. The AI engine in the
  prototype is a transparent heuristic that emulates the trained model for
  demonstration.

---

## 🚀 Getting Started

No installation is required.

1. Download or clone this repository.
2. Open **`index.html`** in any modern web browser (Chrome, Edge, Firefox).
3. Sign in with a demo account, or click **Create account** to register your own.

```bash
git clone https://github.com/<your-username>/fraudguard-ai.git
cd fraudguard-ai
# then just open index.html in your browser
```

### 🔑 Demo accounts

| Username    | Password      | Role          |
|-------------|---------------|---------------|
| `admin`     | `admin123`    | Administrator |
| `researcher`| `research123` | Researcher    |
| `analyst`   | `analyst123`  | Data Analyst  |
| `moderator` | `mod123`      | Moderator     |

You can also create your own account from the **Create account** tab — it is
stored locally in your browser and remembered for next time.

---

## 📁 Project Structure

```
fraudguard-ai/
├── index.html              # The FraudGuard AI prototype (single-file app)
├── README.md               # This file
├── docs/                   # Documentation
│   └── Dissertation.docx   # Full dissertation write-up
├── models/                 # Offline model-training code (Python)
│   ├── preprocess.py       # Text cleaning & tokenisation
│   ├── baselines.py        # TF-IDF + Logistic Regression / Naïve Bayes
│   ├── train_bert.py       # Fine-tuning BERT (Hugging Face Transformers)
│   └── evaluate.py         # Metrics & confusion matrices
├── data/                   # Datasets (not tracked if sensitive)
│   └── .gitkeep
└── assets/                 # Screenshots and figures
    └── screenshots/
```

> Adjust the folders above to match your actual build. The `index.html` file is
> self-contained and can be deployed on its own.

---

## 🧠 Tech Stack

- **Front end:** HTML, CSS, and vanilla JavaScript (single file, no frameworks).
- **Storage:** browser `localStorage` for user accounts and session.
- **Model development (offline):** Python, scikit-learn, and Hugging Face
  Transformers (BERT).
- **Techniques:** Natural Language Processing (NLP), TF-IDF, contextual
  embeddings, and transformer-based text classification.

---

## 🖼️ Screenshots

Place screenshots in `assets/screenshots/` and reference them here, for example:

```markdown
![Login](assets/screenshots/login.png)
![Dashboard](assets/screenshots/dashboard.png)
![AI Detection](assets/screenshots/detection.png)
```

---

## 📊 Model Performance (summary)

| Model                | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression  | 0.862    | 0.851     | 0.874  | 0.862    |
| Naïve Bayes          | 0.821    | 0.803     | 0.842  | 0.822    |
| BERT (fine-tuned)    | 0.948    | 0.948     | 0.948  | 0.948    |

> Figures are drawn from the study's evaluation and should be replaced with your
> final experimental outputs.

---

## ⚠️ Disclaimer

This is a **research prototype** built for academic demonstration. The in-browser
detection is a transparent heuristic simulation; the BERT, Logistic Regression,
and Naïve Bayes models are trained and evaluated separately as described in the
dissertation. It is not a production security tool.

---

## 👤 Author

**ASIFIWE Marie Joyeuse**
Faculty of Business Information Technology, University of Kigali
Supervisor: Dr. MUSABE Jean Bosco

---

## 📄 License

This project is released under the [MIT License](LICENSE). See the LICENSE file
for details.
