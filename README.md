# LLM - PC Game Recommendation Assistant
This project features an AI-powered recommendation assistant that suggests PC games from the Steam store based on user chat queries. It utilizes a Retrieval-Augmented Generation (RAG) pipeline powered by LangChain, Hugging Face transformers, and a FAISS vector database to deliver context-aware, highly-rated game suggestions.

## 🤖 Technologies
* Python
* LangChain
* Hugging Face Transformers
* FAISS
* deep-translator
* pandas

## 💻 Process
* Loaded and merged the Kaggle Steam Store Games dataset and description data using Hugging Face datasets to optimize memory.
* Parsed the dataset into document chunks using RecursiveCharacterTextSplitter for optimal text vectorization.
* Generated text embeddings using the all-MiniLM-L6-v2 model and indexed them into a FAISS vector database.
* Configured a bidirectional translation pipeline to convert queries into English for the model, and the output back into the user's language.
* Implemented an LLM pipeline using the Qwen2-1.5B-Instruct model via LangChain to generate friendly and accurate game recommendations.
* Enhanced the retrieval step by sorting the similarity search results by the highest number of positive reviews before feeding them to the LLM.

## 🎯 Findings
* Successfully built an end-to-end recommendation system capable of understanding user intent and suggesting relevant PC games based on context.
* The integration of translation models allows the system to interact with users seamlessly while querying an English-language dataset.
* Filtering and sorting the FAISS retrieval results by positive ratings significantly improved the quality and reliability of the suggested games.
* The architecture proved to be highly efficient, successfully running lightweight open-source models directly in the notebook environment.
