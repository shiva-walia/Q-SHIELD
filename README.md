# Q-SHIELD — Quantum-Inspired Multi-Domain Financial Fraud Detection System

> A hybrid quantum-classical fraud detection framework that applies quantum superposition and interference-based decision modeling to detect financial fraud across multiple transaction domains.

---

## What This Project Does

Traditional machine learning models for fraud detection face three critical problems:

- **Class imbalance** — fraud is less than 0.2% of transactions, so models learn to ignore it
- **Real-time failure** — most systems flag fraud after the transaction has already completed
- **Binary decisions** — a simple yes/no output cannot handle the uncertainty of real-world fraud

Q-SHIELD addresses all three by representing each transaction as a quantum state vector. Instead of a rigid classification, the system holds multiple possibilities simultaneously and resolves them through a custom interference engine — the same way a human fraud analyst weighs conflicting signals before making a decision.

---

## System Architecture

```
Transaction Data
      │
      ▼
┌─────────────────────┐
│  Data Preprocessing  │  ← SMOTE, normalization, feature scaling
└─────────────────────┘
      │
      ▼
┌─────────────────────┐
│  Quantum State Init  │  ← Amplitude encoding of transaction features
└─────────────────────┘
      │
      ▼
┌─────────────────────┐
│  Interference Engine │  ← Phase shifts based on conflicting signals
└─────────────────────┘
      │
      ▼
┌─────────────────────┐
│  Measurement Module  │  ← State collapse → FRAUD / LEGITIMATE / REVIEW
└─────────────────────┘
      │
      ▼
┌─────────────────────┐
│  Streamlit UI        │  ← Live demo with probability visualization
└─────────────────────┘
```

---

## Fraud Domains Covered

| Domain | Examples |
|--------|---------|
| Credit Card | Unusual amount, location mismatch, merchant anomaly |
| UPI / Digital Payments | Rapid transfers, new device logins, phishing patterns |
| Banking Transactions | Unauthorized wire transfers, account takeover |
| E-Commerce | Fake orders, chargeback fraud, bulk buying patterns |

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.11 | Core language |
| Qiskit | Quantum circuit simulation |
| Scikit-learn | Classical ML baseline models |
| XGBoost | Strong classical comparison model |
| imbalanced-learn | SMOTE for class imbalance |
| Streamlit | Web interface and live demo |
| Plotly | Probability and interference visualizations |
| Pandas / NumPy | Data processing and quantum math |

---

## Dataset

**Kaggle Credit Card Fraud Detection Dataset**
- 284,807 real European credit card transactions
- 492 fraud cases (0.17% of total)
- 30 anonymized features + transaction amount and time
- Source: [kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

---

## Project Structure

```
Q-SHIELD/
├── data/
│   └── creditcard.csv
├── classical/
│   └── classical_models.py       # Logistic Regression, Random Forest, XGBoost
├── quantum/
│   ├── state_initialization.py   # Amplitude encoding of transaction features
│   ├── interference_engine.py    # Phase shift and interference logic
│   └── measurement.py            # State collapse and decision output
├── ui/
│   └── app.py                    # Streamlit web interface
├── results/
│   └── comparison_results.csv    # Classical vs quantum evaluation metrics
├── report/
│   └── daily_notes.txt           # Implementation diary
└── README.md
```

---

## Results

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | — | — | — | — |
| Random Forest | — | — | — | — |
| XGBoost | — | — | — | — |
| Q-SHIELD (Quantum-Inspired) | — | — | — | — |

> Results will be updated as the project progresses.

---

## Research Foundation

This project is backed by peer-reviewed research from IEEE, Springer, and Nature journals:

- Wang et al. (2022) — *Integrating Machine Learning Algorithms with Quantum Annealing Solvers for Online Fraud Detection* — **IEEE Access**
- Huot et al. (2024) — *Quantum Autoencoder for Enhanced Fraud Detection in Imbalanced Credit Card Dataset* — **IEEE Access**
- Biamonte et al. (2017) — *Quantum Machine Learning* — **Nature**
- Havlíček et al. (2019) — *Supervised Learning with Quantum-Enhanced Feature Spaces* — **Nature**
- Kyriienko & Magnusson (2022) — *Unsupervised Quantum Machine Learning for Fraud Detection*

---

## Key Concepts Used

**Quantum Superposition**
Each transaction exists in a superposition of FRAUD and LEGITIMATE states before a decision is made — allowing the system to hold uncertainty rather than forcing a premature binary classification.

**Quantum Interference**
When transaction signals conflict (e.g. large amount from a known merchant), the interference engine applies phase shifts to resolve the conflict probabilistically — modeling how a human analyst weighs multiple signals together.

**Quantum Kernel SVM**
A Support Vector Machine enhanced with quantum feature maps (ZZFeatureMap) that maps transaction data into a higher-dimensional quantum feature space for better classification boundaries.

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/yourusername/Q-SHIELD.git
cd Q-SHIELD

# Install dependencies
pip install -r requirements.txt

# Run the web interface
streamlit run ui/app.py
```

---

## Project Timeline

| Phase | Dates | Status |
|-------|-------|--------|
| Setup + Research | 6–16 May | 🔄 In Progress |
| Classical ML Baseline | 17–23 May | ⏳ Upcoming |
| Quantum Core Engine | 24–30 May | ⏳ Upcoming |
| UI + Integration | 31 May–6 June | ⏳ Upcoming |
| Evaluation + Results | 7–13 June | ⏳ Upcoming |
| Report Writing | 14–27 June | ⏳ Upcoming |
| Final Submission | 28 June–3 July | ⏳ Upcoming |

---

## About

This is my first-ever project as a CSE student — built over 54 days from scratch.

I am documenting the full journey on LinkedIn with weekly progress updates. Feel free to follow along, raise issues, or suggest improvements.

**Connect with me:** [LinkedIn](https://www.linkedin.com/posts/shiva-walia-85407a329_machinelearning-quantumcomputing-frauddetection-share-7459670544674709506-u8LZ?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFLFD0ABwxnaAGWuMZs41n3RiduXAWfwMns)

---

## License

MIT License — free to use, modify, and distribute with attribution.

---

*Built with curiosity, IEEE papers, and a lot of NumPy.*
