Project SHADOW is a simulated AI-powered intelligence assistant designed to respond to RAW agent queries based on classified documents. It leverages document retrieval, semantic search, and role-based agent levels to simulate real-world intelligence workflows.

📌 Features
 
1. Agent Levels: 5 clearance tiers (Novice Operative → Intelligence Overlord) with distinct tones.

2. Doc Ingestion: Upload PDF/DOCX intel manuals for parsing.

3. Vector Search: Uses ChromaDB + OpenAI embeddings for semantic retrieval.

4. Hybrid QA System: Combines LangChain, graph logic, and 100+ rule mappings.

5. Streamlit UI (Optional): Frontend for interactive query simulation.

6. Kaggle-Compatible Notebook: Core logic works with Kaggle-supported libraries.

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

 
