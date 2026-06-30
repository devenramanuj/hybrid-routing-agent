# Hybrid Token-Efficient Routing Agent

A FastAPI-based intelligent routing agent built for the AMD Hackathon. It optimizes LLM usage costs and efficiency by dynamically routing simple queries to a local model (Ollama) and complex or coding tasks to **Gemini 2.5 Flash**.

## Features
- **Smart Logic:** Routes prompts based on length and core coding/mathematical keywords.
- **Fail-safe Fallback:** Seamlessly shifts to Gemini 2.5 Flash if the local server is offline or fails to achieve the confidence threshold.
- **Token Efficiency:** Minimizes high-cost cloud token usage.

## Setup Instructions

### 1. Extract the Project
```bash
unzip routing_agent_final.zip
cd routing_agent
2. Set Environment Variables
Set your Google AI Studio key before running the server:
export GEMINI_API_KEY="your_actual_api_key_here"
3. Run via Docker
docker build -t routing-agent .
docker run -p 8000:8000 -e GEMINI_API_KEY=$GEMINI_API_KEY routing-agent
4. Direct Local Setup (Without Docker)
pip install -r requirements.txt
uvicorn app.main:app --host 0.0.0.0 --port 8000
API Testing
Once started, access the interactive docs at:
http://localhost:8000/docs
