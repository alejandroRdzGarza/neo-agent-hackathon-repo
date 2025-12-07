# Neo Agent Hackathon Repository

Welcome to the **Neo Agent Hackathon Repository**! This project showcases AI-driven tools and agents designed for research assistance, web integrations, and interactive experiences.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Repository Structure](#repository-structure)  
- [Installation](#installation)  
- [Environment Setup](#environment-setup)  
- [Running the Agents](#running-the-agents)  
- [Usage Examples](#usage-examples)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Project Overview

This repository is a collection of AI-based tools and agents developed during a hackathon.  

It includes:  

- **SpoonOS**: A research assistant agent framework using LLMs to help scientists design surveys and process research tasks.  
- **Eleven Labs**: Interactive modules and SDKs for live avatar experiences and web integrations.  
- **Neo**: Core AI modules and utilities that provide agent orchestration and tool management.  

The primary goal is to create intelligent agents that can reason, interact with external APIs, and assist in complex workflows.

---

## Repository Structure

neo-agent-hackathon-repo/
│
├── SpoonOS/ # Research agent framework
│ ├── Neo_Agent_Hackathon/ # LLM integration, agent scripts
│ └── ...
│
├── eleven_labs/ # Interactive avatar and web SDK modules
│ └── cooked/liveavatar-web-sdk/
│
├── neo/ # Core AI modules & utilities
│
├── .gitignore # Git ignore rules
├── Focus.pdf # Hackathon focus and project plan
└── README.md # Project documentation

yaml
Copy code

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/alejandroRdzGarza/neo-agent-hackathon-repo.git
cd neo-agent-hackathon-repo
Create a Python virtual environment:

bash
Copy code
python -m venv spoon-env
source spoon-env/bin/activate  # macOS/Linux
# spoon-env\Scripts\activate    # Windows
Install dependencies:

bash
Copy code
pip install -r SpoonOS/Neo_Agent_Hackathon/requirements.txt
Environment Setup
This project requires API keys for external services. Create a .env file in SpoonOS/Neo_Agent_Hackathon/:

env
Copy code
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
Important: Do not commit .env files to Git. Add them to .gitignore.

Running the Agents
Spoon Research Assistant Agent
Navigate to the SpoonOS folder:

bash
Copy code
cd SpoonOS/Neo_Agent_Hackathon/
Run the research agent:

bash
Copy code
python search_main.py
This will launch a one-shot conversation simulation, where the agent helps design surveys for adults aged 60+.

Eleven Labs Live Avatar SDK
Navigate to the SDK directory:

bash
Copy code
cd eleven_labs/cooked/liveavatar-web-sdk
Follow instructions in the SDK README to launch demo apps.

Usage Examples
Research Agent Example
vbnet
Copy code
🧑‍🔬 Scientist: Hello, I need your help defining a new research survey. We're studying how adults aged 60+ adopt and use modern AI systems like LLMs.

🤖 Assistant: (responds with clarifying questions about demographic scope, technology familiarity, and survey goals)

🧑‍🔬 Scientist: Great. I want the survey to understand motivations, barriers, and patterns of LLM use. What demographics should we capture?

🤖 Assistant: (provides specific demographic categories relevant to older adult technology adoption)

🧑‍🔬 Scientist: Good. Now help me draft 5–7 high-quality questions assessing usage behavior.

🤖 Assistant: (provides 5–7 well-designed survey questions tailored to adults 60+)
The agent can also integrate with other tools, such as web search via the Tavily API, to fetch real-time data for survey support.

Contributing
Contributions are welcome!

Fork the repository

Create a new branch: git checkout -b feature/your-feature

Commit your changes: git commit -m "Add feature"

Push to branch: git push origin feature/your-feature

Open a Pull Request

Ensure no secrets (API keys, .env files) are committed.

License
This project is licensed under the MIT License. See LICENSE for details.

yaml
Copy code

---

I can also **add badges for Python version, build status, and license** to make it look more professional for GitHub.  

Do you want me to do that next?
