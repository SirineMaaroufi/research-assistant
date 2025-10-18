# Research Assistant using Agentic AI

## Overview

This repository contains an experimental AI-powered research assistant built using Ollama for local LLM inference and AutoGen for multi-agent conversations. The assistant interprets research queries, summarizes texts, provides detailed answers, and stores outputs in a JSON file for persistence.

**Important Disclaimer:** This tool is for general research support and experimentation only. It relies on the LLM's internal knowledge, which may not be current or fully accurate. Always verify information with reliable sources for critical work.

## Features

- **Query Agent**: Interprets user tasks and assigns them to appropriate agents.
- **Summary Agent**: Condenses texts (e.g., abstracts) into key insights and saves summaries.
- **Answer Agent**: Delivers detailed responses to questions and stores answers.
- **Storage Agent**: Ensures outputs are properly saved and verified.
- **Persistent Storage**: Saves summaries and answers to a JSON file on Google Drive (in Colab).
- **Local LLM**: Uses Llama 3.2 via Ollama for privacy and offline use.

The project is implemented in a Colab notebook for easy setup and execution.

## Prerequisites

- Python 3.8+
- Ollama installed locally (for LLM inference)
- Google Colab (optional, for Drive integration) or a local Jupyter environment
- Basic libraries: AutoGen, Ollama

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/SirineMaaroufi/ai-research-assistant.git
   cd ai-research-assistant
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
   (See `requirements.txt` for details: autogen[ollama], pyautogen)

3. Install Ollama:
   - Follow the instructions at [ollama.com](https://ollama.com) to install Ollama.
   - Pull the model: `ollama pull llama3.2`

4. (Optional) For Colab: Mount Google Drive for persistent storage.

## Usage

1. Open `research_assistant.ipynb` in Jupyter Notebook or Google Colab.

2. Run the cells step-by-step:
   - Install requirements and mount Drive (if using Colab).
   - Setup environment and start Ollama.
   - Pull the LLM model.
   - Configure agents and start the group chat.

3. Initiate a conversation with a message like: "tell me about agentic ai patterns and the tools that can be used to make ai agents"

Example output from a sample session:
- User: "tell me about agentic ai patterns and the tools that can be used to make ai agents"
- Query Agent: Assigns task to Answer Agent.
- Answer Agent: Explains agentic AI patterns (e.g., tool use, planning) and tools (e.g., AutoGen, LangChain), then saves to `research_outputs.json`.
- Storage Agent: Confirms save.

## Project Structure

- `research_assistant.ipynb`: The main Jupyter notebook with all code and explanations.
- `requirements.txt`: List of Python dependencies.
- `research_outputs.json`: (Generated) Stores summaries, answers, and timestamps (in Google Drive if using Colab).

## Enhancements and Contributions

This is a basic prototype. Potential improvements:
- Add external search integration (e.g., web APIs) for real-time data.
- Develop a web UI (e.g., via Gradio or Streamlit) for better user interaction.
- Include more agents, like a fact-checker.
- Support file uploads for summarizing PDFs or papers.

Contributions are welcome! Please fork the repo, create a feature branch, and submit a pull request. Follow standard Python coding conventions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [Ollama](https://ollama.com) for local AI models.
- Powered by [AutoGen](https://github.com/microsoft/autogen) for multi-agent frameworks.
- Inspired by AI research and agentic systems discussions.

If you have questions or feedback, open an issue on GitHub!
