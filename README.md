# ClarixMind 🔬
### Multi-Agent AI Research System

ClarixMind is a sophisticated multi-agent AI system designed to automate comprehensive web research. Powered by LangChain, Groq (Llama-3.3-70b-versatile), and Tavily, four specialized AI agents collaborate to search, read, write, and critique content, delivering a highly polished research report on any given topic.

## ✨ Features

- **Four Collaborative Agents**:
  - 🔍 **Search Agent**: Gathers recent and relevant web information via the Tavily Search API.
  - 📄 **Reader Agent**: Scrapes and extracts in-depth contextual data from the top resources.
  - ✍️ **Writer Agent**: Drafts a detailed research report tailored to your chosen target audience.
  - 🧐 **Critic Agent**: Reviews, scores, and provides constructive feedback on the generated report.
- **Interactive Chat Interface**: Ask follow-up questions directly to the generated research report.
- **Beautiful UI**: Custom-styled Streamlit interface featuring dynamic progress tracking, pipeline visualization, and step-by-step result viewing.
- **Export Formats**: Seamlessly download the generated report in `.md` (Markdown) or `.pdf` format.

## 🎥 Demo

Watch the multi-agent AI pipeline in action:

<video src="demo.mp4" controls="controls" style="max-width: 100%;">
  Your browser does not support the video tag.
</video>

## 🛠️ Tech Stack

- **Framework**: Streamlit
- **AI & Orchestration**: LangChain, LangGraph
- **LLM Provider**: Groq (`llama-3.3-70b-versatile`)
- **Search API**: Tavily API
- **Web Scraping**: BeautifulSoup4, Requests
- **PDF Generation**: WeasyPrint, Markdown

## 🚀 Getting Started

### Prerequisites
Make sure you have Python installed (3.9+ recommended). You will also need API keys from:
- [Groq](https://console.groq.com/keys)
- [Tavily](https://tavily.com/)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/ClarixMind.git
   cd ClarixMind
   ```

2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows use: env\Scripts\activate
   ```

3. **Install the dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables**:
   Create a `.env` file in the root directory and add your API keys:
   ```env
   GROQ_API_KEY="your_groq_api_key_here"
   TAVILY_API_KEY="your_tavily_api_key_here"
   ```

### Running the App

Run the Streamlit application with the following command:
```bash
streamlit run app.py
```
*The application should now be live on `http://localhost:8501/`*

## 💡 Usage

1. **Enter a Topic**: Type your desired research topic in the text input box (e.g., "Quantum computing breakthroughs in 2025").
2. **Select an Audience**: Choose your target audience (General Public, Academic, 5th Grader, or Executive Summary) to tailor the language and complexity of the report.
3. **Run Pipeline**: Hit "Run Research Pipeline" and watch as the pipeline stages execute dynamically on the UI.
4. **Export or Chat**: Once the Critic Agent finishes its job, you can download the report locally as a Markdown or PDF file, and use the chat section to ask interactive questions based strictly on the report findings.

## 📁 Repository Structure
- `app.py`: Main Streamlit application and UI logic.
- `agents.py`: LangChain setup involving prompts, models, and chains for all 4 agents.
- `tools.py`: Tool definitions mapped to the Tavily search and custom BeautifulSoup web scraper.
- `requirements.txt`: Python dependencies.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.

## 📄 License
This project is open-source and available under the MIT License.
