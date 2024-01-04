

## RAG demo

This respository contains example code for creating and evaluating a Retrieval Augmented Generation (RAG) pipeline with [LangChain[(https://www.langchain.com/) or [Haystack](https://haystack.deepset.ai/) and [Hugging Face](https://huggingface.co/). 


### Data

The example data consists of 440 long PDF documents and meta data from the 2020 open public consultation 
on the EU White Paper on Artificial Intelligence. It is essentially a compilation of 440 position papers on AI regulation in the EU from a wide range of stakeholders. ([Source](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/12270-White-Paper-on-Artificial-Intelligence-a-European-Approach/public-consultation_en)) 

### Example use-cases

1. RAG pipeline with Haystack: 
The notebook `rag_haystack_ai_law.ipynb` contains a basic example for loading, preprocessing, and indexing the data. You can then use a generative LLM like Mixtral to ask questions about stakeholder's positions on AI regulation. 
For example, you can ask the PDFs: "What is Microsoft's position in AI regulation?" or "What are the most important points for civil society regarding AI regulation?" or "What are key risks and benefits of AI?".

2. RAG evaluation with LangChain:
The notebook `rag_langchain_ai_law.ipynb` contains an example for automatic RAG evaluation. It first automatically generates questions with an LLM, then passes these questions into a RAG pipeline and then evaluates RAG response quality with an LLM. 
