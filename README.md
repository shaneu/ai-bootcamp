# AI Bootcamp

The goal of this exercise is to level up my AI engineering skills. I asked ChatGPT 5 to give me a 90 plan and will track
my progress executing that plan here.

## ChatGPT's 90 day plan

## **Phase 1: Foundations (Weeks 1–4)**

**Goal:** Get productive with Python, understand AI concepts, run and integrate your first model.

---

### **Week 1 – Python for Backend Devs (AI-focused)**

**Topics:**

* Python syntax & idioms (for experienced engineers)
* Virtual environments: `venv`, `poetry`
* Async programming with `asyncio` & `httpx`
* Data libraries: `numpy`, `pandas`
* Working with JSON, YAML, and environment configs

**Hands-on:**

* Repo: [realpython/python-scripts](https://github.com/realpython/python-scripts)
* Build a small CLI tool in Python that reads JSON, processes data, and outputs CSV.
* Practice HTTP API calls (e.g., to a public API).

---

### **Week 2 – AI/ML Fundamentals**

**Topics:**

* ML concepts: supervised/unsupervised, embeddings, tokenization
* Transformers 101 (architecture, attention mechanism)
* Prompt engineering basics (few-shot, zero-shot, chain-of-thought)
* APIs: OpenAI & Hugging Face Inference API

**Hands-on:**

* Repo: [huggingface/transformers](https://github.com/huggingface/transformers) (explore examples)
* Call `text-davinci-003` or `gpt-4o` via OpenAI API.
* Experiment with prompt variations to improve output.

---

### **Week 3 – First AI Service**

**Topics:**

* Building APIs with `FastAPI`
* Structuring Python microservices
* Environment variables & secrets (`python-dotenv`)
* Logging best practices for AI apps

**Hands-on:**

* Build a FastAPI service that:

    1. Accepts a question
    2. Calls OpenAI API
    3. Returns the answer
* Deploy locally in Docker
* Repo example: [tiangolo/full-stack-fastapi-postgresql](https://github.com/tiangolo/full-stack-fastapi-postgresql)

---

### **Week 4 – Data for AI**

**Topics:**

* Data ingestion & cleaning (CSV, JSON, PDFs)
* Text preprocessing: tokenization, stemming, stopwords
* Basic vector search concepts

**Hands-on:**

* Use `langchain` to ingest a few Markdown or text docs.
* Convert them to embeddings with OpenAI or Hugging Face models.
* Store vectors in a simple SQLite or in-memory FAISS index.

**Deliverable:**
✅ **Service 1**: “Simple AI Q\&A” (FastAPI + OpenAI API) deployed in Docker.

---

## **Phase 2: Application-Centric AI (Weeks 5–8)**

**Goal:** Build scalable, production-ready AI features (retrieval, orchestration, observability).

---

### **Week 5 – Retrieval-Augmented Generation (RAG)**

**Topics:**

* Chunking strategies
* Vector DBs: pgvector, Weaviate, Pinecone
* Metadata filtering in search

**Hands-on:**

* Repo: [weaviate/weaviate-examples](https://github.com/weaviate/weaviate-examples)
* Build a doc-ingestion pipeline: PDF → chunks → embeddings → vector DB.

---

### **Week 6 – Orchestration & Tool Use**

**Topics:**

* LangChain agents & tools
* Function calling in OpenAI API
* Chaining multi-step workflows

**Hands-on:**

* Create an “AI Research Assistant” that:

    1. Searches the web (SerpAPI tool)
    2. Summarizes results
    3. Returns structured JSON

---

### **Week 7 – Scaling AI Services**

**Topics:**

* Async batch inference
* Redis caching for expensive calls
* Rate limiting & retries
* Cost monitoring (token counting)

**Hands-on:**

* Add caching & metrics to your Service 1 & 2.
* Integrate Prometheus/Grafana for observability.

---

### **Week 8 – Production Deployment**

**Topics:**

* Kubernetes manifests for AI services
* Horizontal Pod Autoscaling (HPA)
* Secrets in K8s (sealed-secrets, external-secrets)

**Hands-on:**

* Deploy Service 2 (“Doc Q\&A with RAG”) to a K8s cluster.
* Load-test with `locust` or `k6`.

**Deliverable:**
✅ **Service 2**: “Doc Q\&A with RAG” deployed to K8s with monitoring & caching.

---

## **Phase 3: Advanced Integration (Weeks 9–12)**

**Goal:** Fine-tuning, hybrid architectures, and end-to-end enrichment workflows.

---

### **Week 9 – Fine-Tuning & LoRA**

**Topics:**

* Dataset preparation for fine-tuning
* LoRA/QLoRA for small, cheap updates
* Hugging Face `Trainer` API

**Hands-on:**

* Fine-tune a small model on a domain dataset (e.g., GitHub issues classification).
* Serve locally via `transformers` pipeline.

---

### **Week 10 – Golang + Python AI Hybrid**

**Topics:**

* gRPC between Go and Python services
* Circuit breaker & retries in Go
* Graceful degradation

**Hands-on:**

* Create a Go microservice that:

    1. Calls the Python AI service
    2. Falls back to cached results if AI is down

---

### **Week 11 – Advanced Vector Search + Enrichment**

**Topics:**

* Hybrid search (BM25 + embeddings)
* Multi-modal embeddings (text + images)
* Entity extraction & tagging

**Hands-on:**

* Build a pipeline that enriches incoming Kafka events with extracted entities from AI.

---

### **Week 12 – Capstone & Polish**

**Topics:**

* Secure API access (JWT/OAuth)
* Documentation & onboarding for other devs
* Cost/performance tuning

**Hands-on:**

* **Capstone Project**:

    * Kafka → Enrichment Service (AI) → NoSQL storage → Query API
    * Deploy to K8s with full CI/CD pipeline

**Deliverable:**
✅ **Service 3**: “AI Workflow Enrichment Service” with streaming input, enrichment, and API output.

---

## **Final Outcomes by Day 90**

1. **Simple AI Q\&A API** (FastAPI + OpenAI API)
2. **Doc Q\&A with RAG** (LangChain + Vector DB) in K8s with caching/monitoring
3. **AI Workflow Enrichment Service** (Kafka + AI processing + Golang integration)

---