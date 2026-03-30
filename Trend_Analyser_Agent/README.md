Analyzer Agent (AI Trends Analysis Pipeline)
A comprehensive AI analysis pipeline that analyzes AI news, benchmarks, and trends. Built using Google's Agent Development Kit (ADK) framework. Full explainer video is available on YouTube. Find more Agent demos built with ADK here

Overview
This agent demonstrates a complex 5-agent sequential pipeline that:

Fetches the latest AI news from Twitter/X using Exa search
Retrieves AI benchmarks and analysis using Tavily search
Scrapes and processes data from Nebius Token Factory using Firecrawl
Synthesizes and structures this information into a comprehensive analysis
Analyzes AI trends and provides specific Nebius model recommendations
Technical Pattern
Uses a 5-agent sequential pipeline:

ExaAgent: Fetches latest AI news from Twitter/X
TavilyAgent: Retrieves AI benchmarks and analysis
SummaryAgent: Combines and formats information from the first two agents
FirecrawlAgent: Scrapes Nebius Token Factory website for model information
AnalysisAgent: Performs deep analysis using Llama-3.1-Nemotron-Ultra-253B model
Installation
Clone the Repo
git clone https://github.com/Arindam200/awesome-ai-apps.git
cd advance_ai_agents/trend_analyzer_agent
Install dependencies:
# Using pip
pip install -r requirements.txt

# Or using uv (recommended)
uv sync
Set up environment variables:
cp .env.example .env
Edit the .env file with your API keys:
NEBIUS_API_KEY="your_nebius_api_key_here"
NEBIUS_API_BASE="https://api.studio.nebius.ai/v1"
EXA_API_KEY="your_exa_api_key_here"
TAVILY_API_KEY="your_tavily_api_key_here"
FIRECRAWL_API_KEY="your_firecrawl_api_key_here"
Usage
Run with ADK CLI:

# Terminal - Run directly in the terminal
adk run analyzer_agent

# Dev UI - Visual interface for testing and debugging
adk web
Required API Keys
Nebius AI - For LLM inference
Exa - For AI news search
Tavily - For specialized search
Firecrawl - For web scraping
