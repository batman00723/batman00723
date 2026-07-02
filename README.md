# Aman Mishra

**AI Application Engineer**  
*Bhopal, India | Final Year CSE @ RGPV University*

[Portfilio](https://portfolio-website-rho-lyart.vercel.app/) | [Email](mailto:batmanmishra23@gmail.com) | [LinkedIn](https://linkedin.com/in/amanmishra232005)

---

# Technical Skills

### Languages
- Python

### Frameworks & Libraries
- Django Ninja
- LangGraph
- LangChain
- Scikit-learn
- SQLAlchemy

### AI / ML
- Large Language Models (LLMs)
- Retrieval-Augmented Generation (RAG)
- Agentic Workflows
- Hybrid Retrieval
- Reranking
- Embeddings

### Databases
- PostgreSQL

### Tools & Concepts
- REST APIs
- Docker
- Git
- Web Scraping (Crawl4AI, Trafilatura)
- Tavily Search API
- Celery
- Redis

### AI Observability & Tracing
- LangSmith

---

# Projects

## AI Receptionist Agent

**Live Demo:** https://ai-receptionist-e48c.onrender.com/api_v1/docs

- Built and deployed an AI Receptionist for dental clinics using LangGraph, automating appointment booking, cancellation, rescheduling, FAQ handling, and emergency escalation.
- Engineered a stateful scheduling workflow with PostgreSQL-backed memory, validation pipelines, and automated IST→UTC conversion for Cal.com integrations.
- Implemented Hybrid RAG with pgvector semantic search and caching, reducing repeated FAQ latency from ~2.8s to ~1.0s while maintaining grounded responses.
- Designed fault-tolerant workflows with automated supervisor email escalation during calendar API failures.
- Integrated Twilio WhatsApp Webhooks, Cal.com scheduling APIs, LangSmith tracing, and PostgreSQL persistence to support production-grade conversational appointment management.

---

## Newsletter Agent

**Subscribe Here:** https://newsletter-yend.onrender.com/

- Built a LangGraph workflow that researches geopolitical events, ranks source relevance, generates newsletters, validates outputs, and delivers reports via email.
- Used LangSmith traces to identify browser scraping as the primary bottleneck; replaced it with Trafilatura HTML parsing, reducing latency ~80% (95s → 15s) and improving P99 tail latency 6x. Cut token usage ~70% (40k → 13k) via content filtering and context-size optimisation, lowering inference cost.
- Implemented an LLM reflection loop to validate generated newsletters against source articles before delivery.
- Scheduled cron job for automated Newsletter delivery via Brevo Email API.

---

## Meeting Analyser

**Live Demo:** https://arvya-meeting-analyser.onrender.com/api_v1/docs

- Designed and deployed a LangGraph-based workflow engine for meeting intelligence, modeling report generation, persistence, and delivery as extensible processing nodes.
- Built a reusable transcript-processing pipeline supporting multiple ingestion paths while maintaining a single analysis layer, reducing workflow duplication and simplifying future integrations.
- Implemented schema-driven LLM extraction with Qwen3-32B and Groq Whisper, converting unstructured audio and transcript data into structured business intelligence artifacts.
- Developed resilient file-processing infrastructure using UUID-prefixed storage, automatic resource cleanup, database persistence, and workflow-level error handling.
- Deployed a production backend on Render with PostgreSQL (Supabase), recipient management APIs, and automated email distribution through Brevo.

---

## RAG Powered Job Matching Agent

- Built an agentic job search pipeline using LangGraph & Django Ninja that autonomously finds, scrapes, and ranks job listings.
- Designed a Hybrid RAG pipeline (semantic search + keyword extraction + Voyage reranking) to score resume-job fit from 0–100.
- Implemented intent routing to classify queries into search or chat flows with automatic query rewriting from chat history.
- Built a self-correcting reflection loop (max_iter=1) to detect LLM hallucinations before surfacing results.
- Engineered stateful persistence via PostgreSQL Checkpointer, preserving session memory across server restarts.
- Integrated Crawl4AI for deep job scraping with a 3-retry + query-rewrite fallback on failed searches.
- Offloaded scraping and LLM inference to Celery + Redis workers for a non-blocking API layer.

---

## Credit Card Default Risk Modelling | 2025

**GitHub:** https://github.com/batman00723/credit_card_default_ml.git

- Engineered behavioural risk signals (delinquency recency, payment discipline, utilisation) from 30K records; excluded demographic features like gender to eliminate bias.
- Benchmarked 3 models; rejected Gradient Boosting despite equal ROC-AUC due to validation instability, selected constrained Random Forest for generalisation reliability.

---

# Education

### B.E. Computer Science & Engineering

**Rajiv Gandhi Proudyogiki Vishwavidyalaya (RGPV), Bhopal**

**Expected Graduation:** 2027

---

## Currently Building AI Systems Focused On

- Autonomous agents
- Retrieval systems
- Real-world automation workflows
