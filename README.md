# RAG-Based Information Extraction for Metal Additive Manufacturing Literature

## Research Goal
This repository implements a Retrieval-Augmented Generation (RAG) framework designed for structured information extraction from Metal Additive Manufacturing (MAM) scientific literature utilizing Large Language Models (LLMs).

## Repository Structure

* `paper_to_process/`: Directory containing the raw input scientific papers in PDF format (currently contains 8 target papers).
* `markdown_outputs/`: Local storage directory for converted Markdown files. This serves as a cache mechanism to save computational resources, ensuring that the PDF-to-Markdown conversion only needs to be executed once per document.
* `1.pdf2metadata.ipynb`: Pipeline for initial document processing and metadata extraction.
* `2.md2llm.ipynb`: Core RAG pipeline for document chunking, semantic retrieval, and LLM-based information extraction.

## Core Modules

### 1. Document Processing & Metadata Extraction (`1.pdf2metadata.ipynb`)
This notebook handles the data ingestion and preprocessing phase.
* **Format Conversion:** Converts the source PDF files located in `paper_to_process/` into structured Markdown (`.md`) format.
* **Caching:** Saves the converted files directly to `markdown_outputs/` for subsequent use.
* **Metadata Extraction:** Utilizes the `gpt-3.5-turbo` API to parse the Markdown content and automatically extract essential document metadata (e.g., Title, Authors, Publication Details).

### 2. RAG Pipeline & LLM Inference (`2.md2llm.ipynb`)
This notebook implements the core retrieval and generation architecture.
* **Document Chunking:** Loads the cached `.md` files from `markdown_outputs/` and segments the text into optimized chunks for embedding.
* **Semantic Retrieval:** Builds the RAG index and executes similarity searches to retrieve the **Top-3** most relevant chunks corresponding to the user query.
* **Prompt Construction:** Engineers a strict, context-aware prompt utilizing the following structure:
  `[TASK] + [CONTEXT (Top 3 Chunks)] + [QUERY] + [RESPOND FORMAT]`
* **Information Extraction:** Feeds the constructed prompt into the target LLM to generate highly grounded and structured responses based on the retrieved MAM literature.

## Getting Started (Workflow)
1. Place the target `.pdf` files into the `paper_to_process/` directory.
2. Execute `1.pdf2metadata.ipynb` to generate the Markdown cache and extract standard metadata. 
3. Execute `2.md2llm.ipynb` to initialize the RAG environment, define your queries, and run the extraction through the LLM.
