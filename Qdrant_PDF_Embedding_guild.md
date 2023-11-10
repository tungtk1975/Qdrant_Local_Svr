# Qdrant PDF Embedding

This Python script demonstrates how to use the Qdrant library to embed text from a PDF file using a BERT-based Sentence Transformer model and store the embeddings in a Qdrant collection.

## Prerequisites

Before running the script, ensure you have the necessary dependencies installed:

- qdrant-client
- pdfplumber
- sentence-transformers

Install the dependencies using:

```bash
pip install qdrant-client pdfplumber sentence-transformers
```

## Usage
**1. Qdrant Server Setup:**

Replace the Qdrant server URL in the script with the URL of your Qdrant server:

```python
qdrant_client = QdrantClient("<your_qdrant_server_url>")
```

**2. PDF File:**

Update the Update the '**pdf_path**' variable with the path to your PDF file:

```python
pdf_path = '/path/to/your/file.pdf'
```
**3. Collection Configuration:**

Update the '**collection_name**' variable to set the name of your Qdrant collection:

```python
collection_name = "your_collection_name"
```

**4. Run the Script:**

Execute the script to embed text from the PDF file into the Qdrant collection:

Just load **Qdrant_local.ipynb** to vscode and enjoy yourself

## Functions
"**extract_text_from_pdf(pdf_path)**'

This function takes a PDF file path as input and extracts text from each page using the '**pdfplumber**' library.

## Embedding and Upserting to Qdrant Collection

The script uses the '**SentenceTransformer**" library to encode text from the PDF into embeddings. These embeddings are then upserted into a Qdrant collection named '**collection_name**'. If the collection does not exist, it will be created.
