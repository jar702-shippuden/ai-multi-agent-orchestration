# 🤖 Multi-Agent Feedback Orchestration with Azure AI Foundry

An AI-powered customer feedback processor built using **Azure AI Foundry**, **GPT-4.1**, and the **agent-framework** library. Three specialized agents run sequentially to automatically summarize, classify, and recommend actions on customer feedback — no manual input required beyond the initial feedback string.

## 🚀 What This Project Demonstrates

- **Sequential Multi-Agent Orchestration** — Three agents run in a pipeline, each building on the previous agent's output
- **Agentic Reasoning** — Each agent autonomously processes its task and passes structured output to the next
- **Azure AI Foundry Integration** — Agents are created and managed via AzureAIAgentClient

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| Azure AI Foundry | AI project infrastructure & model deployment |
| GPT-4.1 | Language model powering the agents |
| agent-framework | SequentialBuilder orchestration |
| Python AsyncIO | Async runtime |
| AzureCliCredential | Secure Azure authentication |

## 📁 Project Structure
```
05-agent-orchestration/
└── Python/
    ├── python agents.py   # Main orchestration script
    ├── requirements.txt   # Dependencies
    └── .env               # Azure credentials (not committed)
```

## 🎯 How It Works

The pipeline processes customer feedback through 3 agents in sequence:

1. **Summarizer** — Condenses feedback into one neutral sentence
2. **Classifier** — Labels it as Positive, Negative, or Feature Request  
3. **Action Agent** — Recommends the next business action

## 💬 Example Output
```
USER FEEDBACK:
"I use the dashboard everyday but the bright screen is harsh on my eyes at night. 
A dark mode option would make it much more comfortable."

------------------------------------------------------------
01 [summarizer]
Customer requests a dark mode option to reduce eye strain when using the dashboard at night.
------------------------------------------------------------
02 [classifier]
Classification: Feature request
------------------------------------------------------------
03 [actions]
Log as enhancement request for product backlog.
```

## ⚙️ Setup

**Prerequisites**
- Python 3.12+
- Azure subscription with AI Foundry access
- Azure CLI authenticated

**Install dependencies**
```bash
pip install -r requirements.txt
```

**Configure environment**

Create a `.env` file:
```
AZURE_AI_PROJECT_ENDPOINT=https://your-project.services.ai.azure.com/api/projects/your-project
AZURE_AI_MODEL_DEPLOYMENT_NAME=gpt-4.1
```

**Run the agent**
```bash
python "python agents.py"
```

*Built with Azure for Students subscription | Spring 2026*
