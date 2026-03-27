# Auto Tagging Support Tickets Using LLM (Zero-Shot vs Few-Shot Learning)

## Objective
The objective of this project is to automatically classify support tickets into predefined categories using a Large Language Model (LLM). The project compares zero-shot and few-shot learning approaches and outputs the top 3 most probable tags for each support ticket.

---

## Dataset
A support ticket dataset containing free-text customer support queries was used.  
Each ticket includes:
- Ticket text
- True category label

**Example Categories:**
- Technical Issue
- Billing Issue
- Account Access
- Subscription
- Delivery Issue

---

## Methodology / Approach

### 1. Zero-Shot Classification
Zero-shot learning was implemented using the Hugging Face model:
```
facebook/bart-large-mnli
```
This model can classify text into categories without prior training by comparing the text with candidate labels.

### 2. Few-Shot Learning
Few-shot learning was implemented using prompt engineering by providing examples and descriptions for each category.  
This helps the model better understand the meaning of each label and improves classification performance.

### 3. Top 3 Tag Prediction
For each support ticket, the model returns:
- Top 1 predicted tag
- Top 2 predicted tag
- Top 3 predicted tag
Along with confidence scores.

### 4. Evaluation Metrics
The models were evaluated using:
- Accuracy
- F1-score
- Classification Report

Zero-shot and Few-shot performance were compared.

### 5. Deployment
A simple web interface was built using **Gradio** where users can enter a support ticket and receive the top 3 predicted tags.

---

## Results / Key Findings
- Zero-shot learning performed well without training data.
- Few-shot learning improved classification performance by providing context and examples.
- Few-shot learning achieved higher Accuracy and F1-score compared to Zero-shot learning.
- The system successfully predicts the top 3 most probable tags for each support ticket.
- This approach can be used in real-world customer support automation systems.

---

## Technologies Used
- Python
- Hugging Face Transformers
- Scikit-learn
- Pandas
- NumPy
- Gradio
---

## How to Run the Project

### 1. Install Required Libraries
```
pip install transformers datasets scikit-learn pandas numpy torch gradio
```

### 2. Run the Notebook
```
jupyter notebook ticket_tagging.ipynb
```

### 3. Run Gradio App
The Gradio interface will launch in your browser where you can input a support ticket and get predicted tags.

---

## Skills Demonstrated
- Prompt Engineering
- Zero-shot Learning
- Few-shot Learning
- LLM-based Text Classification
- Multi-class Prediction
- Model Evaluation
- LLM Application Deployment

---

## Conclusion
This project demonstrates how Large Language Models can be used for automatic support ticket classification using zero-shot and few-shot learning techniques. The results show that few-shot learning improves classification performance by providing context and examples. The system can predict the top 3 most probable categories, making it useful for real-world customer support systems.

---
