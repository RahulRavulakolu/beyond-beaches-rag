# 🌴 Beyond Beaches – RAG AI Assistant

Beyond Beaches is an AI-powered document chatbot built using Retrieval-Augmented Generation (RAG).  
It enables users to upload documents and ask questions to receive accurate, context-aware answers using open-source AI models and automated workflows.

This project demonstrates practical skills in AI engineering, automation, and deployment.

---

## 🚀 Key Features

- 💬 AI-powered conversational interface
- 📄 Automatic document ingestion from Google Drive
- 🔍 Semantic document search using vector embeddings
- 🧠 Context-aware responses using RAG architecture
- ⚙️ Workflow automation with n8n
- 🐳 Docker-based deployment
- 💯 Uses free and open-source AI models

---

## 🏗️ System Architecture

```
User
↓
n8n Chat Interface
↓
Ollama LLM (LLaMA3)
↓
Vector Database (Pinecone - Free Tier)
↓
Google Drive Documents
```

---

## 🛠️ Tech Stack

| Category        | Technology                     |
|-----------------|--------------------------------|
| Automation      | n8n                            |
| LLM             | Ollama (LLaMA3)                |
| Embeddings      | Ollama (nomic-embed-text)      |
| Vector Database | Pinecone (Free Tier)           |
| Storage         | Google Drive API               |
| Deployment      | Docker                         |
| Architecture    | Retrieval-Augmented Generation|

---

## 📌 How It Works

1. User submits a question through the chat interface.
2. The query is converted into vector embeddings.
3. Relevant documents are retrieved from the vector database.
4. Retrieved context is sent to the LLM.
5. The AI generates a precise and relevant response.

This process ensures accurate answers grounded in uploaded documents.

---

## ⚙️ Installation & Setup

### Prerequisites

Make sure you have:

- Docker installed
- Ollama installed
- Pinecone account (Free Tier)
- Google Drive API credentials
- Git

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/beyond-beaches-rag-ai.git
cd beyond-beaches-rag-ai
```

### 2️⃣ Start Services with Docker

```bash
docker compose up -d
```

After startup, open n8n:

```
http://localhost:5678
```

### 3️⃣ Import Workflow

1. Open n8n dashboard
2. Click on Import
3. Upload workflow.json
4. Configure credentials
5. Activate the workflow

### 4️⃣ Configure AI Models

Pull required models:

```bash
ollama pull llama3
ollama pull nomic-embed-text
```

Ensure Ollama is running on:

```
http://localhost:11434
```

---

## 💻 Usage

### Upload Documents

Upload PDF, DOCX, or TXT files to the connected Google Drive folder.

The system automatically processes and indexes them.

### Ask Questions

Open the chat interface in n8n and ask:

```csharp
What is this document about?
Summarize the uploaded file.
Explain page 2 of the PDF.
```

The AI will respond using document-based knowledge.

---

## 📷 Screenshots

Add screenshots inside the `/screenshots` folder:

- Workflow view
- Chat interface
- Execution logs
- Sample responses

Example:

```
screenshots/
 ├── workflow.png
 ├── chat.png
 └── logs.png
```

---

## 📈 Future Enhancements

- Replace Pinecone with self-hosted Qdrant
- Cloud deployment on VPS / Render / Railway
- Web-based frontend (React)
- User authentication
- Multi-document comparison
- Analytics dashboard

---

## 📊 Project Highlights

- Implemented end-to-end RAG pipeline
- Integrated open-source LLMs
- Automated document ingestion
- Designed scalable architecture
- Deployed using containerization
- Optimized for low-cost usage

---

## 👨‍💻 Author

**Rahul Ravulakola**

B.Tech in Artificial Intelligence & Machine Learning

Aspiring AI Engineer & Full Stack Developer

Passionate about building intelligent systems

---

## 📄 License

This project is licensed under the MIT License.

You are free to use, modify, and distribute this project with proper attribution.
