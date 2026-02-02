# LangChain + ChatGroq Streaming Project

This project demonstrates the integration of **LangChain (v1.2.8)** with **ChatGroq models** to build streaming AI applications in Python. It covers **streaming**, **manual streaming**, and **techniques to reduce hallucinations** in large language models (LLMs).

---

## 🛠️ Requirements

- Python version 3.10 or higher  
- `uv` (optional, recommended for isolated project environment)  
- Packages: `langchain`, `langchain-core`, `langchain-community`, `langchain-groq`  

> ⚠️ Do **not** install `langchain-classic` — it breaks streaming imports.  

- Groq API key must be set as an environment variable:
  - Linux/macOS: `export GROQ_API_KEY="YOUR_KEY_HERE"`
  - Windows PowerShell: `setx GROQ_API_KEY "YOUR_KEY_HERE"`

---

## 🔹 Project Structure

The project is organized as follows:

- `streaming_chatgroq.py` — demonstrates streaming using callbacks  
- `manual_stream_chatgroq.py` — demonstrates manual streaming using a for loop  
- `README.md` — project documentation and setup instructions

---

## 🔹 Streaming Options

The project supports two main streaming methods:

1. **Streaming with callbacks:** outputs tokens live using LangChain's built-in streaming handlers. Best for terminal applications and real-time feedback.  

2. **Manual streaming:** outputs tokens manually in a loop without relying on callbacks. Ideal for production environments, APIs, or systems where callback imports may conflict.

---

## 💡 Reducing Hallucinations

Hallucinations occur when LLMs produce **confident but factually incorrect answers**. Best practices include:

- Using a low temperature (e.g., 0) to reduce randomness  
- Providing a system prompt to enforce factual responses  
- Grounding answers with context or external documents  
- Using tools or functions to provide verified factual information  
- Returning structured JSON outputs to minimize guesswork  

---

## ⚡ Notes

- Streaming works best in a terminal environment; Jupyter notebooks may not display tokens live correctly.  
- Manual streaming is more stable in production environments.  
- Always verify your Python environment to avoid `ModuleNotFoundError`.  
- Avoid installing conflicting packages like `langchain-classic`.

---

## 🔮 Next Steps

- Integrate **RAG (Retrieval-Augmented Generation)** to further reduce hallucinations  
- Bind **tools** to answer factual questions  
- Build a **FastAPI or WebSocket streaming chatbot**  
- Use **structured JSON outputs** for downstream applications

---

## 📄 References

- [LangChain Documentation](https://www.langchain.com/docs/)  
- [Groq Model Documentation](https://docs.groq.com/models/)  
- [Research on Reducing Hallucinations in LLMs](https://arxiv.org/abs/2302.13657)
