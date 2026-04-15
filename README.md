# SMILE Explainable Agent

This project implements an AI agent using the Life Programmable Interface (LPI).

## Features
- Connects to LPI MCP server
- Queries multiple LPI tools:
  - smile_overview
  - query_knowledge
  - get_insights
- Uses local LLM (Ollama)
- Provides explainable answers with sources

## Setup Instructions

1. Clone the LPI developer kit:
git clone https://github.com/Life-Atlas/lpi-developer-kit.git

2. Install dependencies:
cd lpi-developer-kit
npm install
npm run build

3. Install Python dependency:
pip install requests

4. Start Ollama:
ollama serve

5. Pull model:
ollama pull qwen2.5:0.5b

6. Run the agent:
python my-agent.py "What is SMILE methodology?"

## Explainability

The agent explicitly lists which LPI tools were used to generate the answer.  
This ensures transparency and reduces hallucination by relying on structured tool data instead of only LLM output.
