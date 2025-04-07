# Clinical Diagnosis RAG Chat

A **Retrieval-Augmented Generation (RAG)** powered chatbot designed for **clinical diagnosis assistance**. This system leverages **FAISS vector search**, **Bio_ClinicalBERT embeddings**, and **LLaMA-3.3-70b** to provide accurate responses based on medical knowledge and patient case studies.

## Features
- **Retrieval-Augmented Generation (RAG)** for improved accuracy
- Uses **Bio_ClinicalBERT** for domain-specific embeddings
- **FAISS** for efficient similarity search
- Supports **clinical diagnosis flowcharts** and **real patient cases**
- **Evaluation module** for measuring retrieval accuracy and response faithfulness

## Tech Stack
- **Frontend**: Streamlit
- **LLM**: LLaMA-3.3-70b via Groq API
- **Embeddings**: Bio_ClinicalBERT
- **Vector Database**: FAISS
- **Backend Processing**: LangChain

---

## Installation

### 1. Clone the Repository
```sh
$ git clone https://github.com/yourusername/clinical-rag-chat.git
$ cd clinical-rag-chat
```

### 2. Set Up a Virtual Environment
```sh
$ python -m venv venv
$ source venv/bin/activate  # Mac/Linux
$ venv\Scripts\activate  # Windows
```

### 3. Install Dependencies
```sh
$ pip install -r requirements.txt
```

### 4. Set Up Environment Variables
Create a `.env` file in the root directory and add:
```
GROQ_API_KEY=your_api_key_here
```

### 5. Run the App
```sh
$ streamlit run app.py
```

---

## File Structure
```
clinical-rag-chat/
│── Diagnosis_flowchart/      # Diagnostic flowcharts (JSON format)
│── Finished/                 # Patient cases categorized
│── app.py                    # Streamlit application
│── evaluation.py              # RAG response evaluation module
│── requirements.txt           # Dependencies
│── .env                       # API key for LLaMA model
│── README.md                  # Project documentation
```

---

## Usage Guide
1. Click the **"🛠️ Initialize System"** button to load the clinical data.
2. Ask questions about patient cases or diagnostic procedures.
3. The chatbot will retrieve relevant documents and generate responses.
4. View **evaluation metrics** (Hit Rate & Faithfulness) to assess the model's accuracy.

---

## Evaluation Metrics
The chatbot includes an **evaluation module** (`evaluation.py`) that measures:
- **Hit Rate**: How often the correct documents appear in the retrieved top-3 results.
- **Faithfulness**: The alignment between generated responses and retrieved context.

These scores help assess response quality and improve retrieval performance.

---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
Special thanks to:
- **LangChain** for seamless LLM integration
- **Hugging Face** for Bio_ClinicalBERT
- **Groq API** for powering LLaMA-3.3-70b
