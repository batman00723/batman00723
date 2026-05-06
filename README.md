# Aman Mishra
**AI & Machine Learning Engineer**  
*Bhopal, India | Final Year CSE @ RGPV University*

[📧 Email](mailto:batmanmishra23@gmail.com) | [🔗 LinkedIn](https://linkedin.com/in/amanmishra232005) | [💻 GitHub](https://github.com/batman00723)

---

# TECHNICAL SKILLS
**Languages:** Python
**Frameworks & Libraries:** Django Ninja, LangGraph, LangChain, Scikit-learn, SQLAlchemy.
**AI / ML:** Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), Agentic Workflows, Hybrid Retrieval, Reranking, Embeddings
**Databases:** PostgreSQL
**Tools & Concepts:** REST APIs, Docker, Git, Web Scraping (Crawl4AI, Trafilatura), Tavily Search API, Celery, Redis
**AI Observability & Tracing:** LangSmith

# PROJECTS

## Newsletter Agent | 2026

**Live Link:** [Click here](https://aman-times-newsletter.up.railway.app/api_v1/docs)  ||    **GitHub:** [Click here](https://github.com/batman00723/Aman-Times-Newsletter.git)

· Deployed a containerised agentic LLM system (LangGraph) that autonomously generates structured newsletters from real-time web data.
· Deployed on Railway free tier with Cerebras free tier — rate limiting under concurrent load is a known issue, fix is a fallback model chain or moving to paid tier.
· Achieved ~75% latency reduction (95s → 25s) and ~6x improvement in tail latency (P99) by eliminating browser scraping and optimizing pipeline execution by replacing browser-based scraping with lightweight HTTP parsing and reducing pipeline bottlenecks and with deliberate model selection — Cerebras Llama 8B (~1000 tokens/sec)
· Cut token usage by ~50% (40k → <15k) by trimming excessive content, lowering inference cost and improving response time.
· Implemented router-based self-correction loop with retry cap (iter≥2) to prevent infinite loops while eliminating hallucinations against source articles.
· Designed asynchronous email dispatch with Celery and Redis background workers; deployment version was simplified to fit free-tier infrastructure limits.
· Added unit tests for LLM pipeline nodes using pytest, mocking LLM and external dependencies to validate system logic and ensure deterministic behaviour.

## RAG Powered Job Matching Agent | 2026

**GitHub:** [Click here](https://github.com/batman00723/Job-Search-Agent/tree/feature/self-correction-loop)

· Architected a multi-node LangGraph pipeline with intent classification, query rewriting, web scraping, and LLM-based resume-to-job matching.
· Built a RAG pipeline from scratch — custom chunking, embedding generation, hybrid retrieval (vector + keyword), and cross-encoder reranking.
· Implemented document ingestion as a decoupled background task using Celery and Redis.
· Integrated Crawl4AI for real-time job page scraping and Tavily for web search with a 3-retry fallback loop on query rewriting.
· Implemented a self-reflection loop where a critique LLM reviews match reports for hallucinations and scoring accuracy before returning results.
· Persisted multi-turn conversation memory using PostgreSQL checkpointing via LangGraph's PostgresSaver.

## Credit Card Default Risk Modelling | 2025

**GitHub:** [Click here](https://github.com/batman00723/credit_card_default_ml.git)

· Engineered behavioural risk signals (delinquency recency, payment discipline, utilisation) from 30K records; excluded demographic features like gender to eliminate bias.
· Benchmarked 3 models; rejected Gradient Boosting despite equal ROC-AUC due to validation instability, selected constrained Random Forest for generalisation reliability.

---

##  Education
*   **B.E. Computer Science & Engineering**
*   **Rajiv Gandhi Proudyogiki Vishwavidyalaya (RGPV)**, Bhopal
*   *Expected Graduation: 2027*

  Currently building AI systems focused on:
- Autonomous agents
- Retrieval systems
- Real-world automation workflows
