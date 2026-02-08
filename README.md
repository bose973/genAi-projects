# 🤖 AI-Powered HR Assistant: Nestlé HR Policy Bot

An intelligent conversational interface designed to parse, understand, and retrieve information from **Nestlé’s HR Policy documents**. This project leverages Retrieval-Augmented Generation (RAG) to provide employees with instant, accurate answers to policy-related questions.

## 🚀 Overview

Navigating dense HR PDF documents can be time-consuming. This project automates that process by:

1. **Extracting** text from official HR policies.
2. **Vectorizing** information for semantic search.
3. **Generating** natural language responses using OpenAI’s GPT models.
4. **Deploying** an intuitive UI via Gradio.

---

## 🛠️ Tech Stack

| Component | Technology |
| --- | --- |
| **Language Model** | OpenAI GPT-3.5 Turbo |
| **Vector Database** | FAISS |
| **Embeddings** | OpenAI Text Embeddings |
| **Framework** | LangChain |
| **Interface** | Gradio |
| **Document Parsing** | PyPDFLoader |

---

## 📋 Features & Workflow

### 1. Data Ingestion & Splitting

Using `PyPDFLoader`, the system reads Nestlé’s HR PDFs. To ensure the AI doesn't lose context or hit token limits, the text is broken down into manageable chunks using a recursive character splitter.

### 2. Vector Storage

Text chunks are converted into numerical vectors (embeddings). These are stored in **FAISS**, allowing the assistant to perform "semantic search"—finding the most relevant policy sections even if the user doesn't use the exact keywords.

### 3. Contextual Prompting

A custom prompt template is used to guide the model. This ensures the assistant:

* Stays professional and helpful.
* Only answers based on the provided document.
* Admits when it doesn't know the answer rather than hallucinating.

### 4. Gradio Interface

A clean, web-based chat interface allows users to type questions and receive real-time responses, making the complex backend tech accessible to any HR staff member or employee.

---

## ⚙️ Setup & Installation

1. **Clone the repository:**
```bash
git clone https://github.com/your-username/nestle-hr-bot.git

```


2. **Install dependencies:**
```bash
conda create -n gen_ai_env python=3.11.13
conda activate gen_ai_env
pip install -r requirements.txt

```


3. **Configure API Key:**
Set your OpenAI API key in your environment variables or within the notebook:
```env file
Open .env file add your api key
OPENAI_API_KEY = "your_api_key_here"

```


4. **Run the Notebook:**
#select gen_ai_env as the kernel for the ipynb file 
Open `Nestle_HR_Assistant.ipynb` and run all cells to launch the Gradio app.
---

## 🎯 Project Result

The final output is a functional `.ipynb` file that demonstrates a full-cycle AI application—from raw PDF data to a live, interactive chatbot.

> **Note:** This tool is designed to assist with policy information. For sensitive personal HR matters, always consult with a human HR representative.