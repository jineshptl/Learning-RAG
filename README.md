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

### Simple LLM calling

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

## Project Structure

```
Learning-RAG/
├── 1_simple_llm_calling/     # Basic LLM invocation examples
├── 2_health_analysis/        # Health/blood work analysis with LLMs
│   └── streamlit_app/        # Streamlit interface
├── .env                      # Your API keys (not tracked)
├── pyproject.toml            # Project dependencies
└── README.md
```

After Adding new folder for 3_vector_db
updated pyproject.toml with chromadb dependency

in terminal run the command below to download all the neccasy package 

```bash
$ uv sync
```

Command below to launch the jupyter notebook

```bash
$ python -m notebook
```