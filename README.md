# Automated Issue Labeling Project

Welcome to my project! This repository contains the code and results for an automated issue classification tool I built, targeting the Python Machine Learning and Data Science ecosystem.

**Developer:** Adnan Qaisar  
**Supervisor:** Dr. Fatima Sabir  
**University:** University of the Punjab  

---
## 📌 Why I Built This

If you've ever looked at massive open-source projects on GitHub like `pandas` or `scikit-learn`, you know their issue trackers are completely overflowing. Maintainers have to manually read and tag thousands of issues as bugs, feature requests, or general questions. It's a huge bottleneck.

For this project, I wanted to see if we could automate this triage process using Natural Language Processing (NLP) and Machine Learning.

## 🛠️ What's in this Repo?

* `Final_Project_Notebook.ipynb`: My complete Google Colab notebook. It covers how I mined the data, cleaned the text, vectorized it, and trained the models.
* `License`: MIT License.
* **Result Graphs:** High-resolution images of my confusion matrices, model comparisons, and feature importance graphs.

---
## ⚙️ How It Works (The Methodology)

Instead of testing on random software, I strictly limited my dataset to 10 major Python ML/DS libraries. I did this so the AI could learn a very specific technical vocabulary. 

* Insert your Methodology Diagram image here *

**Here is the step-by-step process I followed:**
1. **Data Collection:** I used the GitHub API to scrape 10,000 recent issue discussions from projects like PyTorch, Hugging Face Transformers, and MLflow.
2. **Cleaning the Mess:** Real-world GitHub labels are messy. I filtered and merged hundreds of custom tags into three main targets: `bug`, `enhancement`, and `question`.
3. **NLP Vectorization:** I used TF-IDF to turn the raw text into numerical weight vectors.
4. **Training:** I compared a Random Forest ensemble against a Linear Support Vector Machine (SVM) to see which handled the text data better.
