# 🔬 ResearchMind — Multi-Agent AI Research Assistant

ResearchMind is a **Multi-Agent AI Research Assistant** that automates the end-to-end research process using specialized AI agents. Instead of relying on a single language model response, the system coordinates multiple agents that **search the web, extract relevant information, generate a structured research report, and evaluate the quality of the final output**.

Built with **LangChain**, **Groq LLM**, **Tavily Search**, **BeautifulSoup**, and **Streamlit**, the project demonstrates how agent-based AI systems can solve complex tasks through collaboration.

---

## 🚀 Features

* 🤖 Multi-agent architecture with specialized AI agents
* 🔎 Real-time web search using Tavily Search API
* 📄 Intelligent webpage scraping and content extraction
* ✍️ Automated research report generation
* 🧐 AI-powered report evaluation and scoring
* 📥 Download generated reports as Markdown
* 🎨 Modern Streamlit interface with pipeline visualization

---

## 🏗️ System Architecture

```text
                        User Query
                             │
                             ▼
                   ┌──────────────────┐
                   │  Search Agent    │
                   │ (Web Search)     │
                   └────────┬─────────┘
                            │
                            ▼
                   ┌──────────────────┐
                   │  Reader Agent    │
                   │ (Web Scraping)   │
                   └────────┬─────────┘
                            │
                            ▼
                   ┌──────────────────┐
                   │  Writer Chain    │
                   │ Report Generator │
                   └────────┬─────────┘
                            │
                            ▼
                   ┌──────────────────┐
                   │  Critic Chain    │
                   │ Quality Review   │
                   └────────┬─────────┘
                            │
                            ▼
                Final Research Report
```

---

## ⚙️ Workflow

### 🔍 Search Agent

* Searches the web using the Tavily Search API.
* Collects recent and relevant sources.
* Returns article titles, URLs, and summaries.

### 📄 Reader Agent

* Selects the most relevant source.
* Scrapes webpage content using BeautifulSoup.
* Cleans HTML and extracts meaningful text.

### ✍️ Writer Chain

* Combines search results and scraped content.
* Produces a well-structured research report containing:

  * Introduction
  * Key Findings
  * Conclusion
  * Source References

### 🧐 Critic Chain

* Reviews the generated report.
* Assigns a quality score.
* Highlights strengths and weaknesses.
* Provides suggestions for improvement.

---

## 🛠️ Tech Stack

| Category           | Technologies            |
| ------------------ | ----------------------- |
| Language           | Python                  |
| LLM                | Groq (Gemma 2 9B)       |
| Framework          | LangChain               |
| Agent Framework    | LangChain Agents        |
| Search             | Tavily Search API       |
| Web Scraping       | BeautifulSoup, Requests |
| Frontend           | Streamlit               |
| Prompt Engineering | ChatPromptTemplate      |
| Environment        | python-dotenv           |

---

## 📂 Project Structure

```text
ResearchMind/
│
├── app.py                 # Streamlit application
├── agents.py              # AI agents and prompt chains
├── pipeline.py            # Research workflow
├── tools.py               # Search and scraping tools
├── requirements.txt
├── pyproject.toml
├── README.md
└── .gitignore                
```

---

## 🚀 Installation

### Clone the repository

```bash
git clone https://github.com/vaibhaviimahajan/Multi-Agent-System.git
cd Multi-Agent-System
```

### Create a virtual environment

```bash
python -m venv .venv
```

### Activate the environment

**Windows**

```bash
.venv\Scripts\activate
```

**macOS/Linux**

```bash
source .venv/bin/activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

Open your browser at:

```
http://localhost:8501
```

---

## 🎯 Future Improvements

* Multi-source content aggregation
* Citation-aware report generation
* PDF export
* Conversation memory
* Persistent research history
* Parallel agent execution
* Source credibility ranking

---

## 📌 Key Learning Outcomes

This project demonstrates practical experience with:

* Multi-Agent AI Systems
* Agent Orchestration
* Tool Calling
* Prompt Engineering
* Web Search Integration
* Web Scraping
* LLM Pipelines
* AI Report Generation
* AI Self-Evaluation
* Streamlit Application Development

---

## 👩‍💻 Author

**Vaibhavi Mahajan**

GitHub: https://github.com/vaibhaviimahajan
