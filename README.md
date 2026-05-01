# 🏦 Enterprise Multimodal Banking AI Agent

A state-of-the-art, local-first AI assistant designed for secure banking environments. This agent supports **Voice and Text** interactions, performing **RAG (Retrieval-Augmented Generation)** over banking regulations and real-time SQL database queries for user account management[cite: 1, 2].

## 🚀 Features
*   **Multimodal Interaction:** Seamlessly switch between Text and Voice modes[cite: 1, 2].
*   **Local Speech-to-Text (STT):** Powered by OpenAI's **Whisper Medium** for high-accuracy transcription[cite: 1].
*   **On-Device LLM:** Uses **SmolLM2-1.7B** for fast, private, and secure reasoning without external API calls[cite: 1, 2].
*   **Hybrid RAG Architecture:**
    *   **SQL Engine:** Real-time balance and account status checking[cite: 2].
    *   **Vector DB (FAISS):** Semantic search over banking PDFs and policy documents[cite: 2].
*   **Local Text-to-Speech (TTS):** Natural voice responses using **Silero TTS**[cite: 1].
*   **Secure Authentication:** Integrated login system with session management[cite: 2].

## 🛠️ Tech Stack
*   **Models:** OpenAI Whisper (Medium), SmolLM2-1.7B-Instruct, Silero TTS[cite: 1].
*   **Vector Database:** Meta FAISS[cite: 2].
*   **Embeddings:** Sentence-Transformers (all-MiniLM-L6-v2)[cite: 2].
*   **Frameworks:** Transformers, Accelerate, PyTorch[cite: 1].
*   **Database:** SQLite3[cite: 2].

## 💻 Setup & Usage
1.  Open the `BankingAgent.ipynb` in **Google Colab**.
2.  Ensure your runtime is set to **GPU (T4)**[cite: 1].
3.  Run all cells to load models and initialize the database.
4.  Use the following credentials to test the system[cite: 2]:

| Username | Password | Account Type | Balance |
| :--- | :--- | :--- | :--- |
| **Alice** | 1234 | Standard | $5430.00 |
| **Bob** | 1234 | Premium | $25000.50 |
| **Charlie** | 1234 | Blocked | $0.00 |

## 🗣️ Example Queries
*   *"What is my current balance?"* (Queries SQL Database)[cite: 2].
*   *"I lost my card, what should I do?"* (Retrieves from Vector DB)[cite: 2].
*   *"Can I get a loan with my current status?"* (Hybrid Reasoning)[cite: 2].

## ⚠️ Important Note for Colab Users
When using **Voice Mode**, please speak clearly and click the **"Stop"** button immediately after finishing your sentence to ensure the most accurate transcription by Whisper[cite: 1, 2].
