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
