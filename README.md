# Automated Issue Labeling Project

Welcome to my project! This repository contains the code and results for an automated issue classification tool I built, targeting the Python Machine Learning and Data Science ecosystem.

**Developer:** Adnan Qaisar  
**Supervisor:** Dr. Fatima Sabir  
**University:** University of the Punjab  

---
## Why I Built This

If you've ever looked at massive open-source projects on GitHub like `pandas` or `scikit-learn`, you know their issue trackers are completely overflowing. Maintainers have to manually read and tag thousands of issues as bugs, feature requests, or general questions. It's a huge bottleneck.

For this project, I wanted to see if we could automate this triage process using Natural Language Processing (NLP) and Machine Learning.

## What's in this Repo?

* `Final_Project_Notebook.ipynb`: My complete Google Colab notebook. It covers how I mined the data, cleaned the text, vectorized it, and trained the models.
* `License`: MIT License.
* **Result Graphs:** High-resolution images of my confusion matrices, model comparisons, and feature importance graphs.

---
## How It Works (The Methodology)

Instead of testing on random software, I strictly limited my dataset to 10 major Python ML/DS libraries. I did this so the AI could learn a very specific technical vocabulary. 

* Insert your Methodology Diagram image here *

**Here is the step-by-step process I followed:**
1. **Data Collection:** I used the GitHub API to scrape 10,000 recent issue discussions from projects like PyTorch, Hugging Face Transformers, and MLflow.
2. **Cleaning the Mess:** Real-world GitHub labels are messy. I filtered and merged hundreds of custom tags into three main targets: `bug`, `enhancement`, and `question`.
3. **NLP Vectorization:** I used TF-IDF to turn the raw text into numerical weight vectors.
4. **Training:** I compared a Random Forest ensemble against a Linear Support Vector Machine (SVM) to see which handled the text data better.
---

## The Results

I honestly wasn't sure how well classic ML models would handle complex software engineering text, but the results were surprisingly good. 

Both models broke the 90% accuracy barrier. However, **I selected the SVM as my final optimal model.** Why? Because the dataset had a massive class imbalance (way more bugs than questions). The SVM was much smarter at actually finding the rare 'question' category, giving it a better overall balance.


### Looking Inside the AI's Brain
To prove the model wasn't just guessing, I mapped out the highest-weighted words for each category. It turns out the SVM successfully learned the context of software engineering:
* Words like *'bug'*, *'issue'*, and *'fails'* triggered the **Bug** label.
* Words like *'question'*, *'font'*, and *'outcome'* triggered the **Question** label.
## What's Next?

Getting ~90% accuracy with TF-IDF is a great baseline. But because classic ML doesn't understand the full context of a sentence, my next goal for future research is to upgrade this pipeline to Deep Learning. By fine-tuning a transformer model like RoBERTa, I hope to push the accuracy even higher and completely solve the 'question' recall issue. 

## License
This project is open-source and available under the [MIT License](LICENSE).
