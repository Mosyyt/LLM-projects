<div align="center">

# LLM Projects

**A collection of LangChain and OpenAI API projects built while learning how large language models work.**

![Stack](https://img.shields.io/badge/Stack-Python%20%2F%20LangChain%20%2F%20OpenAI-blue?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-Python%203.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)

</div>

---

## What is this?

This repository tracks my learning progress with LangChain and the OpenAI API. Each project comes in two versions: one built using LangChain abstractions, and one written manually directly against the OpenAI SDK — so I can see exactly what the framework is doing under the hood.

---

## Projects

### Chatbot with Memory

A conversational chatbot that retains the full conversation history within a session. The user types messages in a loop and the model responds with full context of everything said before.

| File | Description |
|---|---|
| `chatbot_with_memory.py` | LangChain version using `RunnableWithMessageHistory` and `InMemoryChatMessageHistory` |
| `chatbot_with_memory_manual.py` | Same logic written directly against the OpenAI SDK, no LangChain |

### Debate Agent

An agent that takes a topic, generates structured Pro and Con arguments via separate LLM calls, then summarizes the debate and draws a conclusion.

| File | Description |
|---|---|
| `debate_agent.py` | LangChain chain version |
| `debate_agent_manual.py` | Direct OpenAI SDK version |

---

## Setup

```bash
git clone https://github.com/Mosyyt/LLM-projects.git
cd LLM-projects/chatbot-debate-agent
pip install -r requirements.txt
```

Create a `.env` file in the same folder:

```
OPENAI_API_KEY=sk-...your_key_here
```

---

## Run

```bash
python chatbot_with_memory.py
python debate_agent.py
```

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.10+ | Language |
| LangChain 0.3 | LLM framework and memory management |
| OpenAI API | Language model backend |
| python-dotenv | Load API key from `.env` |
