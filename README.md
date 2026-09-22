# NLP-Project
# Bilingual NLP Company Policy Chatbot

An intelligent bilingual (Arabic & English) semantic search chatbot designed to retrieve company policies and answer employee queries accurately using Natural Language Processing (NLP) techniques.

## Key Features
- Bilingual Support: Processes and responds to both Arabic and English employee queries.
- Arabic Text Normalization: Normalizes Arabic characters (Alef, Teh Marbuta, removal of diacritics) for high text alignment precision.
- Vector Embeddings: Uses sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2 for generating normalized text embeddings.
- Two-Stage Retrieval Architecture: 
  1. Fast Vector Search: Powered by FAISS (IndexFlatIP) with $L_2$ normalization for retrieving top candidate matches.
  2. Cross-Encoder Re-Ranking: Uses cross-encoder/mmarco-mMiniLMv2-L12-H384-v1 to score semantic relevance and ensure exact answer accuracy.

## Tech Stack
- Python 3.12
- Hugging Face Transformers & Sentence-Transformers
- FAISS (Facebook AI Similarity Search)
- Pandas & NumPy

## How to Run
1. Open nlp_company_policy_bot.ipynb in Google Colab or VS Code.
2. Install required dependencies:
   `bash
   pip install transformers sentence-transformers faiss-cpu pandas numpy
