Absolutely! Here's a detailed README specifically for the SpoonOS part of your project, in Markdown format:

# SpoonOS - Research Assistant Agent

SpoonOS is a modular research assistant framework built with AI agents and LLM integration. It is designed to help scientists and researchers design surveys, structure research workflows, and interact with external tools in a seamless, AI-driven environment.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Repository Structure](#repository-structure)  
- [Installation](#installation)  
- [Environment Setup](#environment-setup)  
- [Running the Research Assistant](#running-the-research-assistant)  
- [Usage Example](#usage-example)  
- [Customizing Tools](#customizing-tools)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Project Overview

SpoonOS allows researchers to:

- Generate intelligent survey questions for specific demographics  
- Clarify research goals interactively through an AI agent  
- Use integrated tools for web searches and data retrieval (via the Tavily API)  
- Experiment with multiple LLM providers (OpenAI, Groq, Anthropic)  

The framework follows a **SpoonReactMCP** agent model that allows modular tool integration.

---

## Repository Structure



SpoonOS/
└── Neo_Agent_Hackathon/
├── llm/ # LLM providers, manager, and configuration
├── agents/ # AI agents, including SpoonResearchAssistantAgent
├── tools/ # Tools such as MCPTool and ToolManager
├── chat.py # ChatBot interface for LLMs
├── search_main.py # Main script to run research assistant
├── .env # Environment variables (API keys, etc.) [NOT committed]
└── requirements.txt # Python dependencies


---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/alejandroRdzGarza/neo-agent-hackathon-repo.git
cd neo-agent-hackathon-repo/SpoonOS/Neo_Agent_Hackathon


Create a Python virtual environment:

python -m venv spoon-env
source spoon-env/bin/activate  # macOS/Linux
# spoon-env\Scripts\activate    # Windows


Install dependencies:

pip install -r requirements.txt

Environment Setup

SpoonOS relies on external APIs. Create a .env file with the following keys:

OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key


Important: Do not commit .env files to Git. Add .env to .gitignore.

Running the Research Assistant

Ensure your virtual environment is activated and .env is set.

Run the main script:

python search_main.py


This will start a one-shot conversation simulation where the agent interacts with a simulated scientist to design a survey for adults aged 60+.

Usage Example

Sample interaction:

🧑‍🔬 Scientist: I want to create a survey to study how adults aged 60+ use AI systems like LLMs.

🤖 Assistant: Can you clarify which technology adoption behaviors you want to focus on? Do you want demographics on age, education, or prior AI experience?

🧑‍🔬 Scientist: Focus on motivations, barriers, and usage frequency. Capture age, education, and tech familiarity.

🤖 Assistant: Here are 5–7 survey questions tailored to adults 60+:
1. How often do you use AI systems in your daily life?
2. What motivates you to use AI applications?
3. What challenges or barriers do you face when using AI tools?
...

Customizing Tools

SpoonOS allows integration with additional MCPTools:

from spoon_ai.tools.mcp_tool import MCPTool
from spoon_ai.tools.tool_manager import ToolManager

my_tool = MCPTool(
    name="custom-search",
    description="Custom search tool for research",
    mcp_config={
        "command": "npx",
        "args": ["--yes", "custom-mcp"],
        "env": {"API_KEY": "YOUR_API_KEY"}
    }
)

agent.available_tools = ToolManager([my_tool])


This enables agents to call external services dynamically during conversations.

Contributing

Contributions are welcome!

Fork the repo

Create a new branch: git checkout -b feature/your-feature

Commit your changes: git commit -m "Add feature"

Push branch: git push origin feature/your-feature

Open a Pull Request

Ensure no secrets or API keys are committed.

License

This project is licensed under the MIT License. See LICENSE for details.


---

If you want, I can also **create a shorter, GitHub-friendly version with badges, links to demos, and example screenshots** so it looks really professional for public presentation.  

Do you want me to do that next?
## File Overview - Neo_Agent_Hackathon

Below is a description of the main files in the `Neo_Agent_Hackathon` directory and their purpose:

| File | Purpose |
|------|---------|
| `custom_agent.py` | Contains definitions for custom AI agents that extend the base `SpoonReactMCP` framework. This is where you can implement your own agent logic and specialized behaviors. |
| `search_agent.py` | Implements a search-focused agent that integrates web search tools or APIs. Typically used for retrieving research-related data or survey references. |
| `search_agent_main.py` | The main script to run the search agent. Handles initialization, tool loading, and execution of conversations for search-related tasks. |
| `search_main_one_shot.py` | Demonstrates a **one-shot simulation** of the research assistant agent interacting with a scientist. Useful for testing prompts and agent behavior in a single session. |
| `custom_tool.py` | Defines custom tools that your agents can use. Tools extend the agent’s capabilities, for example, connecting to APIs or performing automated tasks. |
| `tavily_mcp_tool.py` | Implements the Tavily MCP (Modular Command Processor) tool for web searches and automated queries. Allows agents to access external information during a conversation. |
| `tavily_mcp_server.py` | Runs a local server to handle requests from the Tavily MCP tool. Facilitates communication between your agents and the web search API. |
| `spoon-core/` | Core SpoonOS framework files including the LLM manager, provider interfaces, chat functionality, and agent base classes. This is the backbone of your AI agent system. |
| `spoon-env/` | Python virtual environment for the project. Contains installed dependencies and isolated Python packages. **Do not commit this folder.** |
| `main.py` | Entry point for launching your SpoonOS research assistant in full interactive mode. Sets up agents, tools, and LLM providers. |
| `workflow.py` | Defines multi-step agent workflows or task sequences. Useful for chaining tool actions, LLM calls, and structured interactions. |
| `test_search_agent.py` | Unit tests for the search agent to verify that tool integration, prompts, and agent behavior work as expected. Ensures stability during development. |

> **Note:** `.env` files are not included here but are required for API keys. Ensure `.env` files are added to `.gitignore` to prevent accidental pushes of secrets.
