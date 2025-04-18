Project SHADOW is a simulated AI-powered intelligence assistant designed to respond to RAW agent queries based on classified documents. It leverages document retrieval, semantic search, and role-based agent levels to simulate real-world intelligence workflows.

📌 Features
 
 1. Clearance Levels: 5 custom agent tiers from Novice Operative to Intelligence Overlord, each with unique tone and response style.

 2. Classified Document Ingestion: Upload any intelligence manual or case framework PDF/DOCX.

 3. Vector Search with FAISS: Finds semantically relevant context for user queries using vector similarity.

 4. Hybrid Retrieval & Response: Combines graph traversal logic, LangChain-based QA, and predefined rule mappings (100+ rules).

 5. Streamlit Interface: User-friendly frontend for real-time interaction and query simulation.

 6. Kaggle-Compatible Notebook: Uses only Kaggle-supported libraries (no chromadb) with FAISS for vector search.

project structure:

project-shadow/
1. project-shadow.ipynb       ← Main notebook with full implementation
2. .env                        ← API keys and config (local use)
3. README.md                   ← You're reading it
4.  /docs                       ← Supporting intelligence manuals
5. /streamlit_app              ← Optional: Web app for deployment

⚙️ How It Works

1. Upload Intelligence Documents
Documents like SECRET INFO MANUAL.pdf and RAG CASE RESPONSE FRAMEWORK.docx are parsed and chunked for embeddings.

2. Generate Embeddings
Using OpenAI's embedding models (text-embedding-ada-002), each chunk is converted to a vector.

3. Store Embeddings with FAISS
Embeddings are stored in a FAISS index (no chromadb needed — fully Kaggle-compatible).

4. User Query
User inputs a query and selects their agent level (e.g. Level 1: Shadow Footprint).

5. Retrieve Relevant Chunks
The query is embedded and matched to the most relevant document chunks.

6. Apply Rules & Generate Response
Response is generated based on:

Retrieved context
Agent level rules (1–5)

 
