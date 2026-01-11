# Deterministic RAG Agent

A sophisticated Retrieval-Augmented Generation (RAG) system that uses a deterministic graph-based approach to answer complex questions through controlled, multi-step reasoning.

## 🎯 Overview

This project implements a **deterministic RAG agent** that can tackle complex questions requiring multi-step reasoning. Unlike traditional RAG systems that rely on simple semantic similarity, this agent uses a sophisticated graph-based approach to break down complex queries into manageable sub-tasks and execute them systematically.

## ✨ Key Features

- **Deterministic Graph Architecture**: Acts as the "brain" of the agent for complex reasoning
- **Multi-step Reasoning**: Breaks down complex queries into manageable sub-tasks
- **Hallucination Prevention**: Ensures answers are based solely on provided data
- **Adaptive Planning**: Continuously updates plans based on new information
- **Real-time Visualization**: Interactive Streamlit interface for monitoring agent execution
- **Performance Evaluation**: Comprehensive quality assessment using Ragas metrics

## 🏗️ Architecture

The agent follows a deterministic state machine with these key components:

1. **Question Processing**: Anonymize and plan the approach
2. **Task Decomposition**: Break down into retrievable/answerable tasks
3. **Multi-source Retrieval**: Fetch from chunks, summaries, and quotes
4. **Content Verification**: Ensure answers are context-grounded
5. **Adaptive Re-planning**: Update strategy based on new information
6. **Final Generation**: Produce well-reasoned answers

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- OpenAI API key (or other LLM provider)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/Deterministic-Rag-Agent.git
cd Deterministic-Rag-Agent

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys
```

### Usage

1. **Interactive Demo**:
   ```bash
   streamlit run run_agent_simulation.py
   ```
   Visit `http://localhost:8501` to use the web interface

2. **Jupyter Tutorial**:
   ```bash
   jupyter notebook harry_potter_rag_demo.ipynb
   ```

3. **Docker Setup**:
   ```bash
   docker-compose up --build
   ```

## � Use Case: Harry Potter Analysis

The system is demonstrated using the first Harry Potter book to showcase complex reasoning capabilities:

**Example Question**: "How did the protagonist defeat the villain's assistant?"

**Agent Process**:
1. Identify protagonist and villain characters
2. Locate villain's assistant
3. Search for relevant confrontations
4. Analyze defeat circumstances
5. Generate comprehensive answer

## 🛠️ Technology Stack

- **LangChain**: Agent framework and orchestration
- **FAISS**: Vector stores for efficient retrieval
- **Streamlit**: Interactive visualization interface
- **Ragas**: Performance evaluation metrics
- **OpenAI**: Language model integration
- **Pyvis**: Network graph visualization

## 📁 Project Structure

```
Deterministic-Rag-Agent/
├── run_agent_simulation.py      # Main Streamlit application
├── pipeline_functions.py        # Core agent logic and functions
├── helper_functions.py          # Utility functions
├── harry_potter_rag_demo.ipynb  # Step-by-step tutorial
├── graph_visualization.ipynb    # Graph analysis notebook
├── chunks_store/                # Document chunks vector store
├── chapter_summaries_store/     # Chapter summaries vector store
├── book_quotes_store/           # Book quotes vector store
├── requirements.txt             # Python dependencies
└── docker-compose.yml           # Docker configuration
```

## � Core Techniques

1. **Multi-modal Retrieval**: Combines exact matching with semantic search
2. **Query Anonymization**: Removes bias from pre-trained knowledge
3. **Content Distillation**: Improves retrieved information quality
4. **Chain-of-Thought Reasoning**: Step-by-step logical progression
5. **Self-RAG Verification**: Critiques and validates responses
6. **Adaptive Planning**: Dynamic strategy updates

## 📈 Evaluation Metrics

The system is evaluated using Ragas metrics:
- Answer Correctness
- Faithfulness
- Answer Relevancy

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for suggestions and improvements.

---

⭐ If you find this repository helpful, please consider giving it a star!
