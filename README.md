# bedrock-rag-knowledge-base-workshop2
# Hands-on project for AI for Bharat AWS Workshop 2 – Amazon Bedrock Knowledge Bases with RAG
# Multi-Source RAG Knowledge Base using Amazon Bedrock

This repository contains the code and notebooks I used to build a Retrieval Augmented Generation (RAG) application with **Amazon Bedrock Knowledge Bases** as part of the *AI for Bharat – AWS Workshop 2*.

## Features

- Create a Bedrock Knowledge Base with Amazon S3 as a data source
- Use Amazon OpenSearch Serverless as the vector store
- Ingest documents from a synthetic financial dataset
- Retrieve relevant chunks using the `Retrieve` API
- Generate natural language answers using Claude 3 Sonnet via `RetrieveAndGenerate`
- (Optional) Evaluate the RAG pipeline using the **RAGAS** framework
- (Optional) Perform near real-time document updates using the **Document Level API (DLA)**

## AWS Services Used

- **Amazon Bedrock Knowledge Bases**
- **Amazon S3**
- **Amazon OpenSearch Serverless**
- **Amazon Titan Embeddings V2**
- **Claude 3 Sonnet**
- **AWS IAM**
- (Optional) **Amazon SageMaker Studio** for running notebooks

## Notebooks

- `01_create_ingest_documents_test_kb_multi_ds.ipynb`  
  End-to-end: create Knowledge Base, ingest data into S3, run ingestion job, and test retrieval.

- `02_managed_retrieveandgenerate_and_streamapi.ipynb` *(optional)*  
  Managed RAG using RetrieveAndGenerate API and streaming responses.

- `03_customized_rag_retreive_api_hybrid_search_langchain.ipynb` *(optional)*  
  Custom RAG workflow using the Retrieve API and LangChain hybrid search.

- `04_customized_rag_retreive_api_langchain_evaluation_ragas.ipynb` *(optional)*  
  Evaluation of the RAG pipeline using the RAGAS framework.

- `05_document_level_kb_ingestion.ipynb` *(optional)*  
  Near real-time ingestion using Document Level API (DLA).

## How to Run

1. Launch **SageMaker Studio** in the same AWS account where Bedrock is enabled.
2. Clone the original workshop repo or upload these notebooks.
3. Open `01_create_ingest_documents_test_kb_multi_ds.ipynb`.
4. Run the cells from top to bottom:
   - Create S3 bucket, OSS collection, and IAM role
   - Upload synthetic dataset files to S3
   - Run ingestion job
   - Test with the `Retrieve` API
5. (Optional) Explore the other notebooks for advanced features.

## Architecture

At a high level, the solution uses:

- An **Amazon S3** bucket to store documents
- **Amazon Bedrock Knowledge Bases** to manage ingestion, chunking, embeddings, and retrieval
- **Amazon OpenSearch Serverless** as the underlying vector store
- **Claude 3 Sonnet** to generate final answers from retrieved context

## Author

**A. Samuel Arun Kumar**  
Project: *AI for Bharat – AWS Workshop 2 – Building Context-Aware AI Applications with RAG*

