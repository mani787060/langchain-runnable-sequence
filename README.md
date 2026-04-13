# LangChain RunnableSequence Deep-Dive
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green)](https://www.langchain.com/)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Architecture](https://img.shields.io/badge/Architecture-LCEL-orange)](https://python.langchain.com/docs/concepts/#lcel)

## 🏗️ Project Overview
This repository explores the **`RunnableSequence`**, the core primitive that powers the LangChain Expression Language (LCEL). While most developers use the `|` operator, this project takes a step back to look at the underlying class structure. Understanding `RunnableSequence` is essential for building complex, production-ready AI pipelines where you need granular control over how data is passed from one component to the next.

---

## 🛠️ Key Technical Implementations

### 1. Explicit Composition
* **Beyond the Pipe:** Showcasing how to create sequences using `RunnableSequence(first=..., middle=[...], last=...)`.
* **State Management:** Tracking how the input dictionary evolves as it passes through each step of the sequence.

### 2. Standard Runnable Interface
* **Universal Methods:** Demonstrating the power of the Runnable interface:
    * `.invoke()`: Standard synchronous execution.
    * `.batch()`: Processing multiple inputs in parallel for efficiency.
    * `.stream()`: Handling real-time token generation for better UX.

### 3. Custom Logic Injection
* **`RunnableLambda` Integration:** Inserting custom Python functions directly into the sequence to clean data or modify prompts on the fly.
* **Type Safety:** Ensuring that the output of one step matches the expected input of the next.

---

## 💻 Tech Stack
* **Language:** Python 3.9+
* **Orchestration:** LangChain (`langchain-core`)
* **Model:** Google Gemini Pro
* **Environment:** `python-dotenv`

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/langchain-runnable-sequence-mastery.git](https://github.com/your-username/langchain-runnable-sequence-mastery.git)

2. **Install Dependencies:**
   ```bash
   pip install -U langchain-core langchain-google-genai python-dotenv

3. **Setup API Key:**
   Create a .env file in the root directory:
   ```bash
   GOOGLE_API_KEY=your_gemini_key_here

4. **Run the Implementation:**
   ```bash
   python runnable_sequence.py
   
