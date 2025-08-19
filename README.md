# 🧠 Log Classification System using BERT, Regex & DeepSeek LLM

A **hybrid log classification system** that intelligently categorizes log messages using a multi-layered approach:  

- ✅ **Regex** for fast, predictable pattern matching  
- ✅ **BERT embeddings + Logistic Regression** for complex patterns  
- ✅ **DeepSeek LLM (via Groq API)** for edge cases and nuanced logs  

---

## 🔧 Technologies Used

| **Category**              | **Technology / Library**                  | **Purpose**                                      |
|----------------------------|------------------------------------------|-------------------------------------------------|
| Programming Language       | Python 3.11+                              | Core language for processing and modeling      |
| Data Manipulation          | Pandas                                    | Handling and preprocessing log data            |
| Machine Learning           | Scikit-learn                              | Logistic Regression classifier                  |
| NLP / Embeddings           | HuggingFace Transformers, Sentence Transformers | Generate BERT-based embeddings for logs        |
| Large Language Model (LLM) | Groq (DeepSeek LLM)                       | Classifying complex or rare log messages      |
| Rule-based Processing      | Regex                                     | Fast classification for predictable patterns   |
| Environment Variables      | Dotenv                                    | Managing API keys and configuration            |


---

## 🧠 Hybrid Classification Framework

This system implements a **hybrid log classification strategy**, combining three complementary approaches to handle varying log complexity. This ensures high accuracy and flexibility across different log types.  

### 🔹 Classification Approaches

#### ✅ Regular Expression (Regex)
- Fast and effective for **simplified, predictable patterns**.  
- Ideal for logs easily captured with predefined rules.  

#### ✅ Sentence Transformer + Logistic Regression
- Handles **complex patterns** when sufficient labeled data exists.  
- Embeddings generated via **Sentence Transformers (BERT)**.  
- **Logistic Regression** acts as the classifier on embeddings.  

#### ✅ Large Language Model (LLM) via Groq API
- Used when logs are too complex or labeled data is limited.  
- Provides **powerful fallback classification** using DeepSeek LLM.  
- Perfect for **rare edge cases** and nuanced text understanding.  

---

## 🚀 Getting Started

 ```bash
 1️⃣ Clone the Repository

git clone https://github.com/your-username/log-classifier-genai.git
cd log-classifier-genai
python -m venv venv
venv\Scripts\activate  # For Windows
pip install -r requirements.txt

2️⃣ Add .env with your Groq API Key
Create a .env file:
GROQ_API_KEY=your_groq_api_key_here

3️⃣ Run the classifier
Make sure test.csv exists with this structure:
source,log_message
LegacyCRM,Case escalation failed for ticket ID 1234
ModernCRM,User logged in successfully

Then run:
python classify.py
This creates output.csv with predicted labels.

4️⃣ (Optional) Train Your Own Model
jupyter notebook
```

---

✨ Future Enhancements

🌐 Multi-source log integration (servers, cloud apps, IoT)

📊 Dashboard with classification stats

🤖 Real-time log streaming & live classification

🔄 Auto-retraining with new labeled logs

💡 Customizable rules and LLM prompts per project
---
LegacyCRM,Case escalation failed for ticket ID 1234,escalation_error
ModernCRM,User logged in successfully,info
