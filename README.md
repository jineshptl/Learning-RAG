# Learning RAG

A hands-on crash course for learning how to work with LLMs and Retrieval-Augmented Generation (RAG) in Python.

## Setup

### 1. Install UV

```bash
brew install uv
```

### 2. Sync dependencies and create a virtual environment

```bash
uv sync
```

### 3. Activate the virtual environment

**Windows:**
```bash
.venv\Scripts\activate
```

**Linux / Mac:**
```bash
source .venv/bin/activate
```

### 4. Open Jupyter Notebook

```bash
python -m notebook
```

### 5. Add your API key

Create a `.env` file in the top-level folder of the project and add your API key there. This file is git-ignored, so your key will never be committed.

## Usage

### 1. Simple LLM calling

Open `1_simple_llm_calling` and create a new Python Jupyter notebook.

To create an LLM instance, update the model line:

```python
llm = ChatGoogleGenerativeAI(model="<type in your AI model name>")
```

To call the LLM:

```python
response = llm.invoke("How many moons does Jupiter have?")
print(response.text)
```

The same setup applies to both `1_simple_llm_calling` and `2_health_analysis`.

### 3. Vector DB basics

Added a new `3_vector_db` folder to explore vector databases with ChromaDB.

`pyproject.toml` was updated with the `chromadb` dependency. To pull in the new package, run:

```bash
uv sync
```

Then launch Jupyter Notebook as usual:

```bash
python -m notebook
```

### 4. RAG basics

Added a new `4_rag_basics` folder that puts it all together — loading a PDF, chunking it, embedding it into a vector store, and building a retrieval-augmented generation chain.

Same steps as above — sync dependencies, then launch Jupyter:

```bash
uv sync
python -m notebook
```

## Project Structure

```
Learning-RAG/
├── 1_simple_llm_calling/     # Basic LLM invocation examples
├── 2_health_analysis/        # Health/blood work analysis with LLMs
│   └── streamlit_app/        # Streamlit interface
├── 3_vector_db/               # Vector database basics with ChromaDB
├── 4_rag_basics/               # End-to-end RAG pipeline
├── .env                      # Your API keys (not tracked)
├── pyproject.toml            # Project dependencies
└── README.md
```