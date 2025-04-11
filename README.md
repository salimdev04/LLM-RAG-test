# LLM-RAG-test

A local Retrieval-Augmented Generation (RAG) system built with LangChain and Ollama to answer questions about restaurant reviews.

## Overview

This project demonstrates how to build a simple but effective RAG pipeline that:

1. Loads restaurant reviews from a CSV file
2. Embeds the reviews using Ollama's embedding model
3. Stores the embeddings in a local Chroma vector database
4. Retrieves relevant reviews based on user questions
5. Generates contextual answers using LLaMa 3.2 model via Ollama

## Prerequisites

- Python 3.8+
- [Ollama](https://ollama.ai/) installed locally with the following models:
  - `llama3.2` for text generation
  - `mxbai-embed-large` for embeddings

## Installation

1. Clone this repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the main script to start the interactive Q&A session:

```bash
python main.py
```

You can then ask questions about the restaurant reviews. Type `q` to quit the application.

## Project Structure

- `main.py`: The main application that handles user input and generates responses
- `vector.py`: Sets up the vector database and retrieval system
- `restaurants_reviews.csv`: Dataset containing restaurant reviews
- `chroma_langchain_db/`: Directory where the Chroma vector database is stored

## Technologies Used

- [LangChain](https://www.langchain.com/): Framework for developing applications with LLMs
- [Ollama](https://ollama.ai/): Run open-source large language models locally
- [Chroma](https://www.trychroma.com/): Vector database for storing embeddings
- [Pandas](https://pandas.pydata.org/): Data manipulation and analysis
