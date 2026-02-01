# Reflection Agent with LangGraph & Ollama

This project implements a **Reflection Agent** using **LangGraph** and **Ollama**. The agent iteratively generates, evaluates, and refines content (in this case, LinkedIn posts) to improve quality based on self-critique.

## 🚀 Overview

The system uses a graph-based workflow where:
1.  **Generate Node**: Creates an initial draft based on the user's prompt.
2.  **Reflect Node**: Analyzes the draft and provides constructive feedback/critique.
3.  **Iteration**: The agent loops back to the generation node to refine the content based on the critique.
4.  **Termination**: The process stops after reaching a maximum number of iterations (defined by message count).

## 🛠️ Prerequisites

- **Ollama**: Install it from [ollama.com](https://ollama.com).
- **Model**: Pull the Qwen 2.5 7B model:
  ```bash
  ollama pull qwen2.5:7b
  ```

## 📦 Installation

1.  **Clone the repository** (or navigate to the project folder).
2.  **Create and activate a virtual environment**:
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```
3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## 💻 Usage

Run the reflection agent script:
```bash
python3 reflection_agent.py
```

The script will output:
- The initial user request.
- The first AI-generated draft.
- The reflection feedback.
- The final refined version after multiple iterations.

## 🏗️ Architecture

The agent is built using:
- **LangChain**: For LLM orchestration and prompt templates.
- **LangGraph**: To manage the cyclical state and workflow logic.
- **Ollama (Qwen2.5:7b)**: As the local language model.

---
*Based on the Cognitive Class "Building a Reflection Agent with LangGraph" lab.*
