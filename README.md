# 📌 GenAI for Business Analysis  
## Fine-Tuning LLM for Customer Complaint Classification

---

## 🔎 Project Overview

This project demonstrates how to fine-tune a Large Language Model (LLM) to automatically analyze customer complaints and extract structured business insights.

The model extracts:

- **Topic** (department/product)
- **Problem description**
- **Customer Dissatisfaction Index (0–100)**

The goal is to transform unstructured complaint text into structured business intelligence data.

---

## 🎯 Objectives

- Convert raw complaint text into structured insights  
- Fine-tune GPT model on domain-specific data  
- Compare fine-tuned model vs base model  
- Visualize training loss  

---

## 📊 Dataset

**File:** `Customer Complaints.csv`

### Columns:

- `Complaints` → Raw customer complaint text  
- `Details` → Structured expected output (JSON format)  

---

## ⚙️ Methodology

### Step 1: Environment Setup
- Install required libraries  
- Load API key securely  

### Step 2: Data Preparation
- Load CSV dataset using pandas  
- Convert each row into OpenAI fine-tuning format  
- Save as JSONL file  

### Step 3: Upload Dataset
- Upload formatted JSON to OpenAI  

### Step 4: Fine-Tuning
- Fine-tune base model (`gpt-3.5-turbo`)  
- Automatically set training epochs  
- Monitor training progress  

### Step 5: Model Evaluation
- Retrieve training logs  
- Plot training loss graph  
- Compare fine-tuned model vs GPT-4  

### Step 6: Deployment Testing
- Create inference function  
- Extract structured details from new complaints  

---

## 🔄 Input & Output

### ✅ Input

```text
"TV channels keep disappearing from my subscription!"
```

### ✅ Output

```json
{
  "Topic": "TV Subscription",
  "Problem": "Channels Missing",
  "Customer_Dissatisfaction_Index": 85
}
```

---

## 📈 Model Training Monitoring

Training loss is plotted using Matplotlib.

- Decreasing loss → Model is learning properly  
- Stable loss → Convergence achieved  

---

## 🛠 Technologies Used

- Python  
- Pandas  
- OpenAI API  
- JSON  
- Matplotlib  
- python-dotenv  

---

## 💡 Business Impact

This system can:

- Automatically categorize complaints  
- Measure customer dissatisfaction level  
- Help prioritize urgent issues  
- Support business analytics dashboards  
- Improve customer satisfaction tracking  

---

## 🔍 Comparison: Fine-Tuned vs Base Model

| Feature | Base Model | Fine-Tuned Model |
|----------|------------|-----------------|
| Domain Understanding | Generic | Specialized |
| Output Consistency | Moderate | High |
| Business Accuracy | Medium | High |
| Structured Output | Not guaranteed | Reliable |

---

## 📌 Conclusion

This project successfully demonstrates:

- How to fine-tune an LLM  
- How to structure business complaint data  
- How to monitor training loss  
- How to deploy a custom AI model  

Fine-tuning significantly improves:

- Domain accuracy  
- Output consistency  
- Business relevance  
