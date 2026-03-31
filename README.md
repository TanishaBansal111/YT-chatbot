# 🎥 YouTube RAG Chatbot (Ollama Powered)

An AI-powered Retrieval-Augmented Generation (RAG) system that enables users to query YouTube video content using local LLMs via Ollama. Instead of watching long videos, users can ask questions and get precise, context-aware answers instantly.

## 🚀 Features
* **📺 YouTube Video Processing :**
   Extracts and processes transcripts from YouTube videos
* **🧠 RAG-based Q&A System :**
   Answers user queries using Retrieval-Augmented Generation
* **🔍 Semantic Search :**
   Uses FAISS for efficient similarity-based retrieval
* **🤖 Local LLM Integration :**
   Powered by TinyLlama via Ollama
* **🎯 Context-Aware Answers :**
   Generates accurate responses grounded in retrieved content
* **⚡ FastAPI Backend :**
   High-performance API handling with FastAPI
* **💻 Modern Frontend :**
   Responsive UI built with React and Vite
* **🔒 Privacy-Focused :**
   Runs locally without sending data to external APIs
* **💰 Zero API Cost :**
   No dependency on paid AI services
* **⚡ Low Latency :**
   Faster responses due to local processing

## 🛠️ Tech Stack
### 🔹 Backend
* Python
* FastAPI
* FAISS
* Ollama
* TinyLlama
* YouTube Transcript API
* Uvicorn
### 🔹 Frontend
* React
* Vite
* Tailwind CSS
* Axios

## 🧠 How It Works (RAG Pipeline)
### 🔹 1. Data Ingestion
* Extract transcripts using YouTube Transcript API
* Converts video into usable text data
### 🔹 2. Chunking
* Splits transcript into smaller chunks (300–500 tokens)
* Improves retrieval precision and context quality
### 🔹 3. Embeddings
* Converts chunks into vector embeddings
* Captures semantic meaning of text
### 🔹 4. Vector Database
* Stores embeddings using FAISS
* Enables fast similarity-based retrieval
### 🔹 5. Retrieval
* User query → embedding
* Top relevant chunks fetched from FAISS
### 🔹 6. Generation
* Retrieved context + query → passed to TinyLlama via Ollama
* Generates accurate answers with reduced hallucination



<p align="center" style="margin: 50px 0;"><img width="550" height="300" alt="image" src="https://github.com/user-attachments/assets/19f35e03-7544-491d-88db-ad318d1e73a3" /></p>
<p align="center" style="margin: 30px 0;"><img width="550" height="300" alt="image" src="https://github.com/user-attachments/assets/34510b00-3c4a-4c57-97dd-10fb4b5cda7a" /></p>

                                                                                                                 
## 🔧 Installation

### 🔹 1. Clone the Repository
```sh
git clone https://github.com/TanishaBansal111/YT-chatbot.git
cd YT-chatbot
```
### 🔹 2. Backend Setup (FastAPI)
```sh
cd backend
python -m venv venv
venv\Scripts\activate   # for Windows
pip install -r requirements.txt
```
### 🔹 3. Install & Setup Ollama (Local LLM)

Download and install Ollama:

👉 https://ollama.com

Then pull required models:
```sh
ollama pull tinyllama
ollama pull nomic-embed-text
```
Run the model:
```sh
ollama run tinyllama
```
### 🔹 4. Run Backend Server
```sh
uvicorn main:app --reload
```
Backend will run on:

👉 http://127.0.0.1:8000

### 🔹 5. Frontend Setup (React + Vite)

Open a new terminal:
```sh
cd frontend
npm install
npm run dev
```

Frontend will run on:

👉 http://localhost:5173

### 🔹 6. Usage
* Enter a YouTube video URL
* Click Process Video
* Ask questions about the video
* Get AI-generated answers
  
#### ⚠️ Notes
* Ensure Ollama is running before using the app
* Use a system with at least 8GB RAM for smooth performance
* For better accuracy, larger models like llama3 can be used if hardware permits





