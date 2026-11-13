# Enterprise-Grade End-to-End Agentic AI Solution with RAG Architecture

An end-to-end Agentic AI application built on **Databricks**, combining unstructured PDF documents and structured CSV datasets to support context-aware information retrieval and question answering.

The solution explores how an AI agent can use different data retrieval tools, including ranked Vector Search and structured data functions, to answer user queries using relevant information from multiple sources.

## Project Overview

Enterprise information is rarely stored in a single format. Important knowledge can be distributed across technical documentation, product manuals, policies, and structured datasets.

This project brings these sources together in a unified Agentic RAG architecture.

The solution works with:
- **500+ PDF documents:** Unstructured product documentation and knowledge sources.
- **CSV datasets:** Structured information used for data lookup and analytical queries.
- **Databricks Vector Search:** Retrieves relevant document content using vector similarity and ranking.
- **Unity Catalog:** Provides governed access to structured data and callable functions.
- **Agentic AI:** Uses available tools to retrieve information based on the user's query.

## Key Engineering Components

- **Multi-source data ingestion:** Processing PDF documents and structured CSV files.
- **Document processing:** Extracting and preparing PDF content for downstream retrieval.
- **Delta Lake:** Storing structured and processed datasets.
- **Metadata enrichment:** Combining document content with relevant structured information.
- **Vector Search:** Creating searchable indexes and retrieving relevant document passages.
- **Ranked retrieval:** Ordering retrieved results based on relevance.
- **Agent tool integration:** Making document retrieval and structured data functions available to the AI agent.
- **Model deployment:** Using Databricks Model Serving.
- **Observability:** Using MLflow Tracing to inspect agent execution and tool interactions.
- **Application interface:** Providing a conversational interface through Databricks Apps.

## Architecture Overview

The overall workflow follows this sequence:

1. **Data Sources**
   - PDF documents (500+ files)
   - Structured CSV datasets

2. **Data Ingestion and Processing**
   - Extract document content.
   - Process structured datasets.
   - Prepare the data for storage and retrieval.

3. **Data Storage**
   - Store processed datasets in Delta Lake.
   - Organize document content and structured information.

4. **Knowledge Retrieval**
   - Generate embeddings for document content.
   - Create and synchronize Vector Search indexes.
   - Retrieve relevant document passages using ranked search results.
   - Access structured information through Unity Catalog functions.

5. **Agent Orchestration**
   - Receive natural-language queries.
   - Select and invoke relevant tools.
   - Combine retrieved information to formulate a response.

6. **Deployment and Monitoring**
   - Register and deploy the agent through Databricks Model Serving.
   - Track execution using MLflow Tracing.
   - Provide access through a Databricks application.

## Technology Stack

| Area | Technology |
|---|---|
| Cloud Data Platform | Databricks |
| Programming | Python, PySpark, SQL |
| Data Processing | Apache Spark |
| Storage | Delta Lake |
| Data Governance | Unity Catalog |
| Document Retrieval | Databricks Vector Search |
| AI Architecture | Agentic AI, RAG |
| Model Deployment | Databricks Model Serving |
| Observability | MLflow Tracing |
| Application | Databricks Apps |

## Repository Structure

```text
enterprise-grade-agentic-ai-rag/
│
├── notebooks/
│   ├── 01_model_exploration.py
│   ├── 02_pdf_data_ingestion.py
│   ├── 03_structured_data_processing.py
│   ├── 04_document_enrichment.py
│   ├── 05_vector_search_indexing.py
│   ├── 06_agent_tools_and_functions.py
│   └── 07_agent_deployment.py
│
├── sample_data/
│   ├── README.md
│   └── sample.csv
│
├── images/
│   ├── architecture.png
│   ├── application.png
│   └── mlflow_traces.png
│
├── .gitignore
├── requirements.txt
├── LICENSE
└── README.md
```

*Note: The notebook names above are a suggested organization. Replace them with your actual exported notebook names and omit files that you have not implemented.*

## Implementation Workflow

### 1. Foundation Model Exploration

Explore available foundation models on Databricks and understand how to interact with them through supported interfaces.

### 2. PDF Document Ingestion

Process the PDF knowledge base and extract relevant text content for downstream transformation and retrieval.

### 3. Structured Data Processing

Load CSV datasets and prepare structured records for querying through the Databricks environment.

### 4. Metadata Enrichment

Connect relevant document content with structured metadata to preserve context and improve retrieval relevance.

### 5. Vector Search and Ranking

Generate document embeddings, configure Vector Search indexes, and retrieve relevant document passages using the configured ranking approach.

### 6. Agent Tool Integration

Connect the available retrieval mechanisms and structured data functions to the agent so that it can select appropriate tools for user queries.

### 7. Model Registration and Deployment

Register the agent and configure its deployment through Databricks Model Serving.

### 8. Application and Observability

Expose the solution through a conversational application and inspect agent execution using MLflow Tracing.

## Example Use Cases

The application is designed to explore queries that require different kinds of information retrieval:

- Finding specific information from product documentation.
- Retrieving relevant instructions from PDF manuals.
- Looking up information available in structured datasets.
- Answering questions that require combining document context with structured records.

## Setup and Execution

This project was developed using Databricks Free Edition.

To explore the implementation:

1. Clone this repository.
2. Review the notebooks in their execution order.
3. Import the notebooks into your Databricks workspace.
4. Configure the required catalog, schema, volumes, compute resources, and model endpoints.
5. Upload your own permitted source datasets.
6. Execute the ingestion and processing workflows.
7. Configure and synchronize the Vector Search index.
8. Register the required agent tools and deploy the application.

Exact resource names and configurations may need to be adjusted for your Databricks workspace.

## Important Notes

- The original PDF documents and complete source datasets are not included in this repository.
- Databricks workspace resources and model endpoints must be configured separately.
- Cloud resource availability and usage limits depend on the Databricks environment.
- This is an independently maintained implementation based on concepts explored through a public tutorial. Refer to the acknowledgements for the original learning resource.

## Acknowledgements

This project was developed as a hands-on learning and implementation exercise inspired by the tutorial:

**Agentic AI for Beginners: Build an E2E Agentic Solution in Databricks Free Edition**

Original tutorial: https://youtu.be/F7CMlkxHE3o

The repository documents my implementation and learning. Any additional modifications or enhancements are identified separately where applicable.

## Author

**Subhajit Chowdhury**

Data Engineer | AWS Certified | Snowflake

- GitHub: https://github.com/Subhajit-Chowdhury
- LinkedIn: https://www.linkedin.com/in/subhajit-dataengineer/

---

If you find this project useful, feel free to explore the implementation and share your feedback.
