# 🏦 Enterprise Multimodal Banking AI Agent

A state-of-the-art, local-first AI assistant designed for secure banking environments. This agent supports **Voice and Text** interactions, performing **RAG (Retrieval-Augmented Generation)** over banking regulations and real-time SQL database queries for user account management.

## 🚀 Features
*   **Multimodal Interaction:** Seamlessly switch between Text and Voice modes.
*   **Local Speech-to-Text (STT):** Powered by OpenAI's **Whisper Medium** for high-accuracy transcription.
*   **On-Device LLM:** Uses **SmolLM2-1.7B** for fast, private, and secure reasoning without external API calls.
*   **Hybrid RAG Architecture:**
    *   **SQL Engine:** Real-time balance and account status checking.
    *   **Vector DB (FAISS):** Semantic search over banking PDFs and policy documents.
*   **Local Text-to-Speech (TTS):** Natural voice responses using **Silero TTS**.
*   **Secure Authentication:** Integrated login system with session management.

## 🛠️ Tech Stack
*   **Models:** OpenAI Whisper (Medium), SmolLM2-1.7B-Instruct, Silero TTS.
*   **Vector Database:** Meta FAISS.
*   **Embeddings:** Sentence-Transformers (all-MiniLM-L6-v2).
*   **Frameworks:** Transformers, Accelerate, PyTorch.
*   **Database:** SQLite3.

## 💻 Setup & Usage
1.  Open the `BankingAgent.ipynb` in **Google Colab**.
2.  Ensure your runtime is set to **GPU (T4)**.
3.  Run all cells to load models and initialize the database.
4.  Use the following credentials to test the system:

| Username | Password | Account Type | Balance |
| :--- | :--- | :--- | :--- |
| **Alice** | 1234 | Standard | $5430.00 |
| **Bob** | 1234 | Premium | $25000.50 |
| **Charlie** | 1234 | Blocked | $0.00 |

## 🗣️ Example Queries
*   *"What is my current balance?"* (Queries SQL Database).
*   *"I lost my card, what should I do?"* (Retrieves from Vector DB).
*   *"Can I get a loan with my current status?"* (Hybrid Reasoning).

## ⚠️ Important Note for Colab Users
When using **Voice Mode**, please speak clearly and click the **"Stop"** button immediately after finishing your sentence to ensure the most accurate transcription by Whisper.
