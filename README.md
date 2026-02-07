# Policy-QA-Assistant-using-RAG-Prompt-Engineering-LLM-Powered-

A mini **Retrieval-Augmented Generation (RAG)** project that builds a policy-based Question Answering (QA) assistant using **TF-IDF retrieval** and **LLM prompting**, with a strong focus on **hallucination control**, **prompt engineering**, and **safe answer generation**.

---

## 🚀 Project Overview

This project demonstrates how to design a lightweight yet effective RAG pipeline for answering policy-related questions in an enterprise-like setting (NovaCart).  
The system retrieves relevant policy text chunks and constrains the LLM to generate answers **strictly grounded in the provided documents**.

Key goals:
- Prevent hallucinations
- Compare prompt versions
- Handle edge cases gracefully
- Showcase real-world RAG design thinking

---

## 🧠 Key Features

- 📄 Policy document ingestion from `.txt` files  
- ✂️ Text cleaning and chunking with reasoning  
- 🔍 TF-IDF–based retrieval (transparent & interpretable)  
- 🤖 LLM-powered answer generation using **Groq (LLaMA 3)**  
- 🧩 Prompt V1 vs Prompt V2 comparison  
- 🛡️ Hallucination control with safe fallback responses  
- 🧪 Evaluation set and edge-case testing  

---

## 🛠️ Tech Stack

- **Python**
- **Jupyter Notebook**
- **TF-IDF (scikit-learn)**
- **Groq API (LLaMA 3)**
- **NumPy / Pandas**

---

## 🔄 RAG Pipeline Breakdown

1. **Data Loading**  
   Load policy documents from `policy_docs/`.

2. **Text Cleaning**  
   Normalize text (lowercasing, whitespace cleanup).

3. **Chunking Strategy**  
   - ~300-word chunks  
   - Preserves semantic coherence  
   - Avoids context fragmentation

4. **Vectorization**  
   - TF-IDF used for efficient and interpretable retrieval

5. **Retrieval**  
   - Top-k relevant chunks selected per query

6. **Prompt Engineering**
   - **Prompt V1:** Basic instruction-following
   - **Prompt V2:** Strict grounding + hallucination control

7. **Answer Generation**
   - LLM generates answers only from retrieved context

---

## 🧪 Evaluation & Results

| Question | Result |
|--------|-------|
| How long does a refund take? | Correct, policy-grounded |
| Is cash on delivery available? | Information not available |
| What is the warranty period? | Correct |
| Can I cancel after shipping? | Correct |

### Edge Case Test
**Q:** Do you offer international drone delivery?  
**A:** *Information not available in the provided policy documents.*

✔️ Demonstrates effective hallucination prevention.

---

## ⚖️ Design Trade-offs

- **TF-IDF vs Embeddings**  
  TF-IDF was chosen for simplicity, speed, and transparency.  
  Dense embeddings could improve semantic recall but add complexity.

- **Chunk Size**  
  Larger chunks preserve meaning but reduce retrieval precision.

---

## 🔮 Future Improvements

- Hybrid retrieval (TF-IDF + embeddings)
- Cross-encoder re-ranking
- Automatic evaluation metrics (e.g., faithfulness)
- UI integration (Streamlit / Gradio)
- Multi-document citation highlighting

---

## 📌 Why This Project Matters

This project mirrors **real-world GenAI systems** where:
- Accuracy matters more than creativity
- Hallucinations are unacceptable
- Prompt design is a core engineering skill

It showcases practical RAG knowledge suitable for **AI/ML Engineer Intern** and **GenAI-focused roles**.

---

### 🔐 API Key Setup
This project uses the Groq API for LLM access.

To test it yourself:
1. Create a free Groq account → [https://console.groq.com](https://console.groq.com)
2. Generate an API key.
3. Set it as a system environment variable:
   - **Windows (CMD):**
     ```bash
     setx GROQ_API_KEY "your_api_key_here"
     ```
   - **Mac/Linux:**
     ```bash
     export GROQ_API_KEY="your_api_key_here"
     ```
4. Restart Jupyter Notebook and run the chatbot.


## 👤 Author    
Chinta Harichandan    
📧 Email: harichandan130505@gmail.com  
🔗 LinkedIn Profile: https://www.linkedin.com/in/harichandan-chinta-210451346  
📂 GitHub: https://github.com/ChintaHariChandan  

## 📜 License
This project is licensed under the MIT License – feel free to use, modify, and distribute.



