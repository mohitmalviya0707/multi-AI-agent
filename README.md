# 🤖 Multi-Agent Research System

An intelligent research automation pipeline built with LangChain that uses multiple specialized agents to search, scrape, analyze, and critique research on any given topic. The system generates structured, high-quality research reports with automated feedback loops.

---

## ✨ Features

- **🔍 Intelligent Search Agent**: Uses Tavily API to find recent, reliable information from the web with title, URL, and snippet extraction.
- **📄 Smart Scraping Agent**: Extracts clean text content from URLs, removing scripts, styles, and navigation elements for focused reading.
- **✍️ Professional Writer Chain**: Generates well-structured research reports with introduction, key findings, conclusion, and sources.
- **🎯 Critical Analysis Chain**: Evaluates the generated report with scoring, strengths, areas for improvement, and a verdict.
- **🔄 Complete Pipeline Orchestration**: End-to-end automation from topic input to final critiqued report.
- **📊 Rich Console Output**: Beautiful, formatted terminal output using the `rich` library.

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|------------|
| **Framework** | LangChain |
| **LLM** | OpenAI GPT-4o-mini |
| **Search API** | Tavily API |
| **Web Scraping** | BeautifulSoup4 + Requests |
| **Output Formatting** | Rich Library |
| **Environment Management** | Python-dotenv |

---

## 📋 Prerequisites

- Python 3.9 or higher
- OpenAI API key
- Tavily API key

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/multi-agent-research.git
cd multi-agent-research



┌─────────────┐
│ User Input  │
│   (Topic)   │
└──────┬──────┘
       │
       ▼
┌─────────────────┐
│  Search Agent   │ ← Tavily API
│ (Web Search)    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Reader Agent   │ ← Web Scraping
│ (URL Scraping)  │   (BeautifulSoup)
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Writer Chain   │ ← GPT-4o-mini
│ (Report Gen)    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Critic Chain   │ ← GPT-4o-mini
│ (Evaluation)    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Final Output    │
│ (Report + Score)│
└─────────────────┘
