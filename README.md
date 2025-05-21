# RAG Chatbot with LangChain

This project implements a Retrieval-Augmented Generation (RAG) chatbot using the [LangChain](https://www.langchain.com/) framework and OpenAI's language models. It leverages FAQ data, stores it in a vector database (FAISS), and allows for intelligent question-answering.

## 🚀 Features

- **LangChain Integration**: Uses LangChain to build a modular and scalable chatbot.
- **FAISS Vector Store**: Stores document embeddings for efficient semantic search.
- **OpenAI GPT Model**: Generates human-like answers based on retrieved context.
- **CSV-based Knowledge Base**: Uses structured FAQ data from CSV files.

## 📂 Project Structure

```

rag-chatbot-langchain/
│
├── data.csv                # Dataset used for chatbot context
├── faq\_data.csv            # Structured FAQ data
├── main.ipynb              # Jupyter notebook for model implementation
├── README.md               # Project documentation
└── anaconda\_projects/      # (Optional) Anaconda environment/project metadata

````

## ⚙️ Installation

1. **Clone the Repository**:
   ```bash
   git clone <repo-url>
   cd rag-chatbot-langchain
````

2. **Install Dependencies**:
   Run the first cell of `main.ipynb` or manually install:

   ```bash
   pip install langchain openai faiss-cpu tiktoken pandas
   ```

3. **Set your OpenAI API Key**:
   You can set it in the environment or directly in the notebook:

   ```python
   os.environ["OPENAI_API_KEY"] = "your-api-key"
   ```

## 🧠 How It Works

1. Loads FAQ data from `faq_data.csv`.
2. Converts text into embeddings using OpenAI's embedding model.
3. Stores embeddings in a FAISS vector store.
4. Uses LangChain retriever and chain to generate answers for user questions.

## 💡 Example

Ask:

> What is Deep Learning?

Response:

> Deep Learning is a subset of ML that uses neural networks.

## 📌 Requirements

* Python 3.8+
* OpenAI API key
* Jupyter Notebook
