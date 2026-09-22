# 🤖 AI Fluency Training

### Student: Dineshkumar K

### Program: B.Tech Artificial Intelligence & Data Science

---

## 📌 Project Overview

This project demonstrates the difference between a **Plain LLM Chatbot**, a **Rule-Based Workflow**, and an **AI Agent with Tools**.

The project uses a college course-fee scenario to demonstrate how different AI systems handle information, rules, tools, and decision-making.

The main goal is to understand:

* How a basic LLM chatbot works
* How rule-based workflows work
* How AI agents use tools
* Why LLMs can hallucinate when they don't have access to private data
* How tools can provide reliable information to an AI agent

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand the basics of LLM-based applications.
2. Build a simple chatbot using an LLM.
3. Create a deterministic rule-based workflow.
4. Build an AI agent that can call external tools.
5. Compare the strengths and limitations of each approach.
6. Understand the importance of reliable data sources.
7. Demonstrate tool calling and agent loops.

---

## 🧠 Systems Demonstrated

### 1. Plain Chatbot

The first system is a normal LLM chatbot.

It receives a question and sends it directly to the language model.

```text
User
 ↓
LLM
 ↓
Response
```

The chatbot does **not** have access to the private course-fee data.

Therefore, questions involving private data may result in incorrect or guessed answers.

---

### 2. Rule-Based Workflow

The second system uses predefined programming rules.

```text
User Question
      ↓
Extract Course Code
      ↓
Retrieve Fee
      ↓
Apply Rules
      ↓
Final Answer
```

The workflow is predictable and reliable for the questions it was specifically designed to handle.

However, it can fail when the user asks a question in an unexpected way.

---

### 3. AI Agent

The third system combines an LLM with tools.

```text
             User Question
                   ↓
                AI Agent
                   ↓
          ┌────────┴────────┐
          ↓                 ↓
   Course Fee Tool     Calculator Tool
          ↓                 ↓
          └────────┬────────┘
                   ↓
              Final Answer
```

The agent can decide which tool is required and use the returned information to generate an answer.

---

# 🛠️ Technologies Used

* **Python**
* **OpenAI Python SDK**
* **python-dotenv**
* **Ollama**
* **Qwen 2.5 1.5B**
* **VS Code**
* **Python Virtual Environment**
* **LLM Tool Calling**

---

# 📂 Project Structure

```text
day1_lab/
│
├── .env
├── .gitignore
├── requirements.txt
│
├── config.py
├── check_setup.py
├── chatbot.py
├── workflow.py
├── tools.py
├── agent.py
├── challenge.py
│
└── .venv/
```

### File Description

| File               | Purpose                                                   |
| ------------------ | --------------------------------------------------------- |
| `config.py`        | Configuration, LLM provider, model and course data        |
| `check_setup.py`   | Checks Python, model and LLM connection                   |
| `chatbot.py`       | Implements the plain LLM chatbot                          |
| `workflow.py`      | Implements the rule-based workflow                        |
| `tools.py`         | Contains tools available to the AI agent                  |
| `agent.py`         | Implements the tool-using AI agent                        |
| `challenge.py`     | Tests a question not explicitly designed for the workflow |
| `.env`             | Stores provider and model configuration                   |
| `.gitignore`       | Prevents `.env` from being uploaded                       |
| `requirements.txt` | Lists required Python packages                            |

---

# 📊 Sample Course Data

The project uses the following fictional course-fee data:

| Course Code |     Fee |
| ----------- | ------: |
| CS101       | ₹12,000 |
| AI202       | ₹18,000 |
| DS303       | ₹15,000 |

This data is stored locally and is not automatically known by the LLM.

---

