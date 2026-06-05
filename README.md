# AI Engineering — Study Notes
**Handwritten study guide | GoodNotes**

---

## Contents

1. **Large Language Models**
   - What are LLMs
   - Popular LLMs (GPT-4o, Gemini, Claude)
   - Use cases

2. **SOTA Models**
   - SOTA LLM Timeline (2020 → 2025)
   - Frontier LLMs
   - Reasoning Models
   - Small / Efficient Models
   - Coding Models
   - SOTA Image Generation Models
   - Video Generation + Multimodal

3. **Transformer Architecture**
   - Tokenization + BPE
   - Positional Encoding + RoPE
   - Attention mechanism + formula
   - Softmax + saturation
   - Time & space complexity
   - Long context fixes (Flash Attention, Sliding Window)

4. **Key-Value Cache**
   - Why KV cache exists
   - What it grows with
   - Optimisations: PagedAttention, Prefix Caching, Sliding Window
   - MHA vs MQA vs GQA

5. **Fine-Tuning**
   - Full training pipeline (6 stages)
   - Data & instruction formatting
   - LoRA — Low-Rank Adaptation
   - QLoRA — Quantized LoRA
   - NF4 quantization
   - Memory comparison (fp32 → fp16 → int8 → NF4)

6. **Chunking Strategies**
   - Fixed size
   - Recursive
   - Semantic
   - Document-aware
   - Parent-child
   - Late chunking

7. **RAG — Retrieval-Augmented Generation**
   - Naive RAG pipeline (ingestion + query phases)
   - Embeddings + similarity metrics
   - Vector databases (pgvector, Pinecone, Weaviate, Chroma, Qdrant)
   - HNSW indexing

8. **Advanced RAG**
   - Pre-retrieval: Query rewriting, HyDE, Multi-query, Step-back, RAG Fusion, Query decomposition
   - Retrieval: Hybrid search (BM25 + vector + RRF), Metadata filtering, SPLADE
   - Post-retrieval: Reranking, Contextual compression, Lost-in-the-middle fix
   - Agentic RAG: Self-RAG, Corrective RAG, Adaptive RAG, Iterative RAG
   - GraphRAG, Multimodal RAG, Modular RAG

9. **RAG in Production**
   - Ingestion pipeline (incremental + async)
   - Serving (semantic caching, streaming, parallel retrieval)
   - Cost control (token budgeting, model tiering)
   - Index freshness (scheduled, event-driven, soft delete)
   - Top production failure modes

10. **Prompt Engineering**
    - Prompt anatomy (role → instructions → format → context)
    - Zero-shot, Few-shot, Chain-of-Thought
    - Structured output
    - Role prompting
    - Grounding + citation instructions
    - Good vs bad prompt (side by side)
    - Temperature + generation parameters

11. **Hallucination — Detection & Reduction**
    - Types: Intrinsic, Extrinsic, Factual
    - Layer 1: Retrieval quality
    - Layer 2: Prompt design (grounding, CoT + self-check)
    - Layer 3: Generation parameters
    - Layer 4: Output detection (NLI, SelfCheckGPT, LLM-as-judge, web grounding)
    - Layer 5: Architecture patterns (RAG, abstention, schema validation)

12. **RAG Evaluation**
    - Retriever metrics: Context Precision, Context Recall, Context Relevancy, Precision@K, Recall@K, MRR, NDCG
    - Generator metrics: Faithfulness, Answer Relevancy, Answer Correctness, Answer Completeness, BLEU/ROUGE, BERTScore, G-Eval
    - When to use which (production monitoring vs release gating)
    - Eval tools: RAGAS, LangSmith, MLflow, DeepEval, UpTrain

13. **LLM Agents**
    - Core definition + Agent formula
    - Perceive → Think → Act loop
    - ReAct pattern
    - Memory types (in-context, external, episodic, semantic, shared)
    - Types of agents (reflex → autonomous)
    - Tool use + function calling
    - Multi-agent patterns (orchestrator, sequential, parallel, DAG, critic, debate)
    - Frameworks: LangGraph, LlamaIndex, CrewAI, AutoGen
    - Agent evaluation (5 layers)
    - Safety & reliability metrics

14. **MCP — Model Context Protocol**
    - What MCP solves
    - Architecture (host, client, server)
    - 3 primitives (tools, resources, prompts)
    - Transport (stdio vs HTTP + SSE)
    - Origin (Anthropic Nov 2024) + ecosystem

15. **LLM Deployment**
    - 4 deployment modes (API, self-hosted, managed, edge)
    - Serving frameworks: vLLM, TGI, Ollama
    - Continuous batching + PagedAttention
    - Speculative decoding
    - Tensor parallelism
    - TTFT + TPOT
    - Quantization (INT8, INT4, AWQ, GPTQ)
    - Scaling strategies (horizontal, model gateway, autoscaling)

16. **Voice Agents**
    - Full pipeline (VAD → STT → LLM → TTS)
    - Latency budget
    - STT models (Deepgram, Whisper, AssemblyAI)
    - TTS models (ElevenLabs, Cartesia, OpenAI TTS)
    - Latency optimisations (streaming, barge-in, filler words)
    - End-to-end speech models (GPT-4o Realtime)
    - Frameworks (LiveKit, Pipecat, Twilio)

17. **LLM Observability**
    - Observability vs evaluation
    - Traces + spans
    - What to log per span (LLM, retrieval, tool)
    - Tools: LangSmith, Arize Phoenix, Helicone, Langfuse
    - Metrics to monitor + alert thresholds
    - Debugging workflow
    - Drift detection
    - OpenTelemetry standard

---

*Made with GoodNotes on iPad*
