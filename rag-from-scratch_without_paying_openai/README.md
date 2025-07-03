# RAG From Scratch
## Updates in This Fork

- **OpenAI Embeddings Replaced:** All OpenAI embedding calls have been replaced with [Qwen3-Embeddings](https://ollama.com/library/qwen3-embedding-0.6b) via Ollama for fully local, free, and privacy-friendly vectorization.
- **Chat Model:** Google's lightweight [Gemma3:1b](https://ollama.com/library/gemma3) is used for chat and generation, also running locally via Ollama.
- **Issues Solved:**
  - ChromaDB telemetry warnings suppressed and explained.
  - Retrieval chain errors with `.map()` replaced by robust explicit retrieval logic.
  - Duplicate function and variable errors fixed.
  - Submodule and git issues resolved for clean repo usage.
  - YoutubeLoader and transcript issues addressed (see notebook comments for versioning tips).
- **Thanks:**
  - Special thanks to the original author and [LangChain](https://github.com/langchain-ai/rag-from-scratch) for the excellent learning resources and foundational code.

---

## Using Ollama for Local Embeddings and Chat

1. **Install Ollama:**
   - Download and install from [https://ollama.com/download](https://ollama.com/download)
2. **Start Ollama server:**
   - Run `ollama serve` in your terminal.
3. **Pull required models:**
   - For embeddings: `ollama pull dengcao/Qwen3-Embedding-0.6B:Q8_0`
   - For chat: `ollama pull gemma3:1b`
4. **Run the notebooks:**
   - All code will use these local models for embedding and chat.

------------


LLMs are trained on a large but fixed corpus of data, limiting their ability to reason about private or recent information. Fine-tuning is one way to mitigate this, but is often [not well-suited for factual recall](https://www.anyscale.com/blog/fine-tuning-is-for-form-not-facts) and [can be costly](https://www.glean.com/blog/how-to-build-an-ai-assistant-for-the-enterprise).
Retrieval augmented generation (RAG) has emerged as a popular and powerful mechanism to expand an LLM's knowledge base, using documents retrieved from an external data source to ground the LLM generation via in-context learning. 
These notebooks accompany a [video playlist](https://youtube.com/playlist?list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x&feature=shared) that builds up an understanding of RAG from scratch, starting with the basics of indexing, retrieval, and generation. 
![rag_detail_v2](https://github.com/langchain-ai/rag-from-scratch/assets/122662504/54a2d76c-b07e-49e7-b4ce-fc45667360a1)
 
[Video playlist](https://www.youtube.com/playlist?list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x)

---

## Credits
- Original author: [LangChain RAG from Scratch](https://github.com/langchain-ai/rag-from-scratch)
- This fork: Qwen3-Embeddings and Gemma3:1b integration, bugfixes, and local-first improvements.