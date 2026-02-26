# 🤖 Multi-Agent Feedback Orchestration with Azure AI Foundry

An AI-powered customer feedback processor built using **Azure AI Foundry**, **GPT-4.1**, and the **agent-framework** library. Three agents run sequentially to process feedback automatically.

## 🚀 What It Does

1. Takes a customer feedback string as input
2. **Summarizer agent** condenses it into one sentence
3. **Classifier agent** labels it as Positive, Negative, or Feature Request
4. **Action agent** recommends the next step

## 🛠 Tech Stack

- Azure AI Foundry
- agent-framework SequentialBuilder
- Python asyncio
- AzureCliCredential auth
