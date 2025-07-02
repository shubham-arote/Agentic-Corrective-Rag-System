## 🛠️ Key Components

### 1. **Vector-Based Document Retrieval**
- Uses **ChromaDB** to store and query vector-embedded documents.
- Embeds incoming user queries and retrieves top-k semantically similar documents.

### 2. **Relevance Grading Engine**
- Applies semantic similarity scoring (e.g., cosine similarity).
- Automatically grades retrieved documents based on a dynamic relevance threshold.

### 3. **Auto-Agentic Query Correction**
- If retrieved context is irrelevant or weak:
  - System **autonomously rewrites** the query using an internal agent.
  - Initiates **web search** with the corrected query for broader coverage.

### 4. **Context Augmentation via Web Search**
- Extracts and appends relevant web search snippets to the original context.
- Deduplicates and filters low-quality or off-topic results.

### 5. **Context-Constrained Response Generation**
- Generates answers **strictly using retrieved and verified context**.
- If no sufficient context is available, the system abstains from answering or asks for clarification.
- **No hallucinations** — only grounded, traceable responses.

---

## ✅ Key Features

- ✅ **Self-correcting pipeline** with autonomous query rewriting and fallback logic.
- ✅ **Hybrid context** blending local vector retrieval and live web search results.
- ✅ **Context-grounded generation**: outputs are strictly based on retrieved material.
- ✅ **Dynamic relevance scoring** ensures precision and minimizes noise.
- ✅ **Modular design**: each component can be independently scaled or swapped.
- ✅ **Hallucination-resistant**: avoids speculative responses without solid grounding.
- ✅ **Scalable** to multiple domains (technical, medical, legal, etc.).
