# 🤖 Multi-Agent AI Research System

An AI-powered research automation application that uses specialized AI agents to search the web, extract relevant information, generate structured research reports, and evaluate report quality.

Built with **Python, LangChain, LangGraph, OpenRouter, Tavily, and Streamlit**, this project demonstrates how AI agents and external tools can collaborate to automate an end-to-end research workflow.

## ✨ Features

- 🔎 **Automated Web Search** — Retrieve relevant web results using the Tavily Search API.
- 📄 **Intelligent Content Extraction** — Extract readable text from web pages using Requests and BeautifulSoup.
- ✍️ **AI-Powered Report Generation** — Generate structured research reports with introductions, key findings, conclusions, and sources.
- 🧐 **Automated Report Critique** — Evaluate generated reports with scores, strengths, and improvement suggestions.
- 🧩 **Multi-Agent Architecture** — Coordinate specialized search and reader agents through LangChain.
- 🔌 **Flexible LLM Integration** — Access supported language models through OpenRouter.
- 🖥️ **Interactive Web Interface** — Use Streamlit to interact with the research application.

## 🏗️ System Architecture

```text
                 Research Topic
                       |
                       v
              +------------------+
              |  Streamlit UI    |
              +------------------+
                       |
                       v
              +------------------+
              |   Search Agent   |
              |  Tavily Search   |
              +------------------+
                       |
                       v
              +------------------+
              |   Reader Agent   |
              |  Web Scraping    |
              +------------------+
                       |
                       v
              +------------------+
              |   Writer Chain   |
              | Report Generation|
              +------------------+
                       |
                       v
              +------------------+
              |   Critic Chain   |
              | Report Evaluation|
              +------------------+
                       |
                       v
                Research Report
                 + Feedback
```

## 🔄 How It Works

1. **Topic Input:** The user enters a research topic through the Streamlit interface.
2. **Web Search:** The Search Agent retrieves relevant web pages, URLs, and snippets using Tavily.
3. **Content Extraction:** The Reader Agent identifies a relevant URL and extracts additional information.
4. **Report Generation:** The Writer Chain combines the collected research into a structured report.
5. **Quality Evaluation:** The Critic Chain evaluates the report and provides a score, strengths, and areas for improvement.
6. **Results Presentation:** The application presents the research output through its user interface.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Interactive web interface |
| LangChain | Agent creation and LLM orchestration |
| LangGraph | Agent execution framework |
| OpenRouter | Language model API access |
| Tavily Search API | Web search and information retrieval |
| Requests | HTTP requests |
| BeautifulSoup | HTML parsing and text extraction |
| python-dotenv | Environment variable management |

## 📁 Project Structure

```text
Multi-Agent-AI-Research-System/
│
├── app.py              # Streamlit web application
├── agents.py           # Search and reader agents, writer and critic chains
├── pipeline.py         # Research workflow orchestration
├── tools.py            # Web search and web scraping tools
├── requirements.txt    # Python dependencies
├── .env                # API keys (not committed)
├── .gitignore          # Git exclusions
└── README.md           # Project documentation
```

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.10 or later
- An OpenRouter API key
- A Tavily API key
- Git

### 1. Clone the repository

```bash
git clone https://github.com/MousumiBadyakar/Multi-Agent-AI-Research-System.git
cd Multi-Agent-AI-Research-System
```

### 2. Create and activate a virtual environment

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Get your API keys from:

- [OpenRouter](https://openrouter.ai/settings/keys)
- [Tavily](https://app.tavily.com/)

**Security:** Never commit your `.env` file or expose API keys in your source code.

### 5. Run the Streamlit application

```bash
streamlit run app.py
```

Streamlit will display a local URL in your terminal. Open it in your browser to use the application.

To run the terminal-based research pipeline separately:

```bash
python pipeline.py
```

## 📑 Research Report Structure

The generated report is designed to include:

- **Introduction** — Background and context for the topic.
- **Key Findings** — At least three detailed findings.
- **Conclusion** — Summary of the major insights.
- **Sources** — URLs identified during the research process.

The Critic Chain separately provides a score out of 10, strengths, areas to improve, and a one-line verdict.

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `OPENROUTER_API_KEY` | Authenticates language model requests |
| `TAVILY_API_KEY` | Authenticates web search requests |

The project is configured to use OpenRouter's `openrouter/free` model router. Model availability, tool-calling support, and free usage limits depend on the available models and your account.

## 🚧 Current Limitations

- Research quality depends on the retrieved sources and selected language model.
- Some websites may block automated scraping or return incomplete content.
- Free model availability and API limits may affect execution.
- The current research pipeline executes its stages sequentially.
- Generated reports may require manual fact-checking and source verification.

## 🔮 Future Enhancements

- Deploy the Streamlit application publicly.
- Add application screenshots and a live demo link.
- Support downloadable reports in PDF and Markdown formats.
- Improve source verification and citation validation.
- Add configurable models and robust retry handling.
- Introduce parallel agent execution to reduce research time.
- Add automated tests for the research pipeline and its components.

## 🎯 Learning Outcomes

This project explores practical applications of:

- Multi-agent AI system design
- LLM integration and tool calling
- LangChain and LangGraph orchestration
- Automated web research and content extraction
- AI-powered report generation and evaluation
- Streamlit application development
- API key and environment configuration

## 👩‍💻 Author

**Mousumi Badyakar**
