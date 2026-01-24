# LangChain Document Loaders

This folder contains hands-on implementations of **document loaders in LangChain**, which are a core building block for Retrieval-Augmented Generation (RAG) systems.

Document loaders are responsible for loading data from different sources and converting it into LangChain’s standardized `Document` format, which can then be used for text splitting, embeddings, retrieval, and generation.

---

## Why Document Loaders Matter

In RAG-based applications, data can come from many sources:

- Text files
- PDFs
- CSV files
- Web pages
- Entire directories of documents

LangChain document loaders provide a consistent way to ingest this data so that downstream components can work seamlessly.

This folder focuses on understanding:
- How different loaders work
- What kind of `Document` objects they produce
- How metadata and content are structured
- When to use eager loading vs lazy loading

---

## Files in This Folder

### Text and File-Based Loaders
- `text_loader.py`  
  Loads plain text files and converts them into `Document` objects.

- `pdf_loader.py`  
  Demonstrates loading PDF files using PyPDFLoader, with one document per page.

- `csv_loader.py`  
  Loads CSV files where each row becomes a separate `Document`.

---

### Directory-Based Loading
- `directory_loader.py`  
  Loads multiple documents from a directory (e.g., many PDFs or text files at once) using pattern matching.

---

### Web-Based Loading
- `webbase_loader.py`  
  Loads and extracts text content from web pages using WebBaseLoader.

---

## Supporting Files

- `cricket.txt`  
  Sample text file used for text loader demonstrations.

- `GenAI-LLMs.pdf`  
  Sample PDF used for PDF loader examples.

- `Social_Network_Ads.csv`  
  Sample CSV dataset used for CSV loader demonstrations.

- `books/`  
  Directory containing multiple PDFs used to demonstrate directory-based loading.

---

## Key Concepts Demonstrated

- Standardized `Document` objects
- Page content vs metadata
- Loading from different data sources
- Directory-based ingestion
- Lazy loading vs eager loading
- Preparing data for downstream RAG components

---

## Next Steps

The output of document loaders is typically used for:
- Text splitting
- Embedding generation
- Vector database storage
- Retrieval pipelines

Covered in subsequent retrieval system folders.
