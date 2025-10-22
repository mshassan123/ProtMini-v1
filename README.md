# ProtMini v1

![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](LINK_TO_YOUR_NOTEBOOK)

## 🔬 Overview

**ProtMini v1** is a **lightweight, universal protein function prediction tool** designed for researchers and bioinformaticians. It leverages **pretrained ESM2 embeddings** and an **ensemble of classifiers** (MLP, Logistic Regression, Random Forest) to predict the functional class of any protein sequence.

This tool can:
- Fetch **real reviewed sequences** from UniProt.
- Generate **high-dimensional embeddings** using ESM2.
- Predict protein function with multiple classifiers.
- Provide **confidence scores** and second-best predictions.
- Export **professional PDF reports** summarizing results.

---

## ⚡ Features

- **Universal Classification:** Covers enzymes, transporters, signals, structural proteins, immune proteins, and unknown “other” sequences.
- **Ensemble Approach:** Combines deep learning (MLP) and classical ML (Logistic Regression & Random Forest) for reliable predictions.
- **PDF Reports:** Automatic, timestamped reports for reproducibility and presentation.
- **GPU-Accelerated Embeddings:** Fully compatible with **Google Colab GPU**, speeding up large dataset embeddings.
- **Custom Sequence Input:** Predict your own protein sequences easily via a text box in Colab.

---

## 🛠 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/protmini.git
cd protmini
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Or directly in Colab:

python
Copy code
!pip install transformers torch biopython reportlab tqdm scikit-learn ipywidgets
🚀 Usage
Open the notebook protmini_colab.ipynb in Google Colab.

Paste your protein sequence into the text box.

Click "Predict Function".

Wait for embeddings and predictions.

Download your PDF report from the outputs/ folder.

Example Output:

bash
Copy code
🧩 Predictions: {'MLP': 'enzyme', 'LogReg': 'enzyme', 'RandomForest': 'signal'}
📊 Confidences: {'MLP': 0.87, 'LogReg': 0.83, 'RandomForest': 0.79}
🔗 2nd-best classes: {'MLP': 'signal', 'LogReg': 'signal', 'RandomForest': 'enzyme'}
🧬 Methodology
Data Fetching: Real, reviewed protein sequences are retrieved from UniProt for different functional classes. A set of random sequences is added as “other”.

Embedding Generation: Each sequence is encoded using ESM2, a state-of-the-art protein language model, producing high-dimensional embeddings.

Classifier Training:

MLP (Deep Learning)

Logistic Regression

Random Forest

The ensemble ensures both robustness and accuracy.

Prediction & Report: User-provided sequences are embedded and run through all classifiers. The predictions, confidences, and second-best classes are summarized in a PDF report.

📁 Repository Structure
bash
Copy code
protmini/
│
├─ protmini_colab.ipynb       # Main Colab notebook
├─ requirements.txt           # Dependencies
├─ README.md
├─ LICENSE
├─ outputs/                   # Generated PDF reports
└─ utils/                     # Optional: helper scripts
    ├─ fetch_sequences.py
    └─ embedding_utils.py
⚙️ Future Improvements
Batch predictions for multiple sequences.

Save/load embeddings to speed up repeated runs.

Add interactive visualization of embedding clusters.

Extend classification to cover more protein families.

📚 References
UniProt

ESM2 Protein Language Model

PyTorch & scikit-learn libraries

📝 License
This project is licensed under the MIT License – see the LICENSE file for details.

👨‍💻 Author
Muhammad Sohaib Hassan
