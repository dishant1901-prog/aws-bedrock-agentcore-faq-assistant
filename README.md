# 🤖 AWS Bedrock AgentCore AI FAQ Assistant with Persistent Memory

An AI-powered FAQ Assistant built using **AWS Bedrock AgentCore Runtime**, **LangGraph**, **LangChain**, **FAISS**, **FastEmbed**, **Groq LLM**, and **Amazon Bedrock AgentCore Memory**.

The assistant performs semantic search over a custom FAQ knowledge base using Retrieval-Augmented Generation (RAG) while maintaining long-term conversational memory across user sessions.

---

## 🚀 Features

- ✅ AI-powered FAQ Assistant
- ✅ Semantic Search using FAISS Vector Database
- ✅ FastEmbed Embeddings for lightweight deployment
- ✅ Groq GPT-OSS-20B Large Language Model
- ✅ LangGraph Agent with Tool Calling
- ✅ AWS Bedrock AgentCore Runtime Deployment
- ✅ Amazon Bedrock AgentCore Memory Integration
- ✅ Long-Term User Memory
- ✅ Multi-tool Retrieval Workflow
- ✅ Production-ready Cloud Deployment

---

## 🏗️ Architecture

```
                   User
                     │
                     ▼
        AWS Bedrock AgentCore Runtime
                     │
                     ▼
              LangGraph Agent
                     │
      ┌──────────────┼──────────────┐
      │              │              │
      ▼              ▼              ▼
 FastEmbed       FAISS Vector     Groq LLM
 Embeddings       Database      (GPT-OSS-20B)
                     │
                     ▼
         AgentCore Persistent Memory
```

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python 3.13 |
| Framework | LangGraph |
| Agent Framework | LangChain |
| Embeddings | FastEmbed |
| Vector Database | FAISS |
| LLM | Groq (GPT-OSS-20B) |
| Cloud Runtime | AWS Bedrock AgentCore |
| Persistent Memory | AWS Bedrock AgentCore Memory |
| Dependency Management | UV |
| Deployment | Docker + AWS Bedrock AgentCore |

---

## 📂 Project Structure

```
.
├── 00_langgraph_agent.py
├── 01_agentcore_runtime.py
├── 02_agentcore_memory.py
├── lauki_qna.csv
├── pyproject.toml
├── uv.lock
├── README.md
├── .sample_env
└── .gitignore
```

---

## ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/dishant1901-prog/aws-bedrock-agentcore-faq-assistant.git

cd aws-bedrock-agentcore-faq-assistant
```

Install dependencies

```bash
uv sync
```

---

## 🔑 Environment Variables

Create a `.env` file using `.sample_env` as reference.

```env
HF_TOKEN=your_huggingface_token
GROQ_API_KEY=your_groq_api_key
MEMORY_ID=your_agentcore_memory_id
```

---

## ▶️ Run Locally

### LangGraph Agent

```bash
uv run python 00_langgraph_agent.py
```

### AgentCore Runtime

```bash
uv run python 01_agentcore_runtime.py
```

### AgentCore Memory

```bash
uv run python 02_agentcore_memory.py
```

---

## ☁️ Deploy to AWS Bedrock AgentCore

Deploy the runtime using AgentCore Toolkit.

```bash
agentcore launch
```

Invoke the deployed runtime

```bash
agentcore invoke '{"prompt":"Tell me about roaming activation."}'
```

---

## 💬 Example Queries

- Explain roaming activation.
- What roaming packs are available?
- How do I activate international roaming?
- What happens after my roaming pack expires?
- Tell me about data roaming.

---

## 🧠 Persistent Memory Example

User:

```
My name is Dishant.
```

Later:

```
What is my name?
```

The assistant retrieves the stored information using **Amazon Bedrock AgentCore Memory** and responds with the remembered user information.

---

## 📸 Demo

A complete demonstration of the project is available on my LinkedIn profile.

The demo showcases:

- Semantic FAQ Retrieval
- AWS Bedrock AgentCore Runtime Deployment
- AgentCore Memory Integration
- Long-Term Memory Retrieval
- Cloud Deployment Workflow

---

## 📈 Challenges Solved

During development, several practical deployment challenges were addressed:

- Docker image exceeded AWS AgentCore runtime size limits.
- Replaced SentenceTransformers with FastEmbed to significantly reduce deployment size.
- Integrated persistent memory using Amazon Bedrock AgentCore Memory.
- Configured LangGraph agents for production deployment.
- Built a lightweight semantic retrieval pipeline optimized for cloud deployment.

---

## 🔮 Future Improvements

- Hybrid Search (Keyword + Semantic)
- Streaming Responses
- Multi-Agent Collaboration
- Authentication & User Profiles
- Web Interface using Streamlit
- Amazon Bedrock Guardrails Integration
- MCP Tool Support

---

## 📚 Technologies Used

- AWS Bedrock AgentCore Runtime
- AWS Bedrock AgentCore Memory
- LangGraph
- LangChain
- FAISS
- FastEmbed
- Groq API
- Python
- Docker
- UV Package Manager

---

## 👨‍💻 Author

**Dishant Kaushik**

GitHub:
https://github.com/dishant1901-prog

LinkedIn:
(Add your LinkedIn profile here)

---

## ⭐ If you found this project useful

Please consider giving the repository a ⭐ on GitHub.
