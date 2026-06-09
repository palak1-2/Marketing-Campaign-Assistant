# Marketing Campaign Assistant (Multi-Agent AI System)

An AI-powered multi-agent marketing system built using **Google ADK (Agent Development Kit)** and Python.
The system automates the creation of a complete marketing campaign brief by orchestrating multiple specialized LLM agents.

---

## 📌 Overview

This project implements a **sequential multi-agent pipeline** where each agent is responsible for a specific stage of marketing campaign creation.

A user provides a product idea, and the system generates a complete marketing strategy including:

* Market research insights
* Core messaging strategy
* Ad copy variations
* Visual concept suggestions
* Final structured campaign brief

---

## 🧠 Architecture

The system uses a **Sequential Agent Orchestration pattern**.

### Flow:

Market Research Agent
→ Messaging Strategist
→ Ad Copy Writer
→ Visual Suggester
→ Campaign Formatter

Each agent passes its output to the next using shared state keys.

---

## ⚙️ How It Works

### 1. Market Research Agent

* Uses Google Search tool via ADK
* Extracts market trends, competitors, and target audience insights
* Stores output in `state["market_research_summary"]`

### 2. Messaging Strategist Agent

* Builds core messaging and value propositions
* Uses research insights as input
* Outputs to `state["key_messaging"]`

### 3. Ad Copy Writer Agent

* Generates platform-specific ad copies (Tweet, Social Post, Headline)
* Uses messaging as input
* Outputs to `state["ad_copy_variations"]`

### 4. Visual Suggester Agent

* Suggests marketing visuals aligned with ad copy
* Outputs to `state["visual_concepts"]`

### 5. Formatter Agent

* Combines all outputs into a structured Markdown campaign brief
* Produces final output in `state["final_campaign_brief"]`

---

## 🗂️ Project Structure

```text id="mcx91a"
Marketing-Campaign-Assistant/
│
├── agent.py          # Multi-agent orchestration logic (SequentialAgent)
├── instructions.py   # Prompt definitions for all agents
├── __init__.py       # Package initialization
```

---

## 🧩 Key Concepts Used

* Multi-Agent Systems (MAS)
* Sequential Agent Orchestration
* LLM Prompt Engineering
* State-based communication between agents
* Tool usage (Google Search via ADK)
* Modular agent design

---

## 🛠️ Tech Stack

* Python
* Google ADK (Agent Development Kit)
* Gemini / LLM models
* Google Search Tool integration
* dotenv for environment configuration

---

## 🚀 Example Use Case

**Input:**

> "A new AI-powered fitness tracking app for students"

**Output:**

* Market demand and competitor insights
* Target audience segmentation (students, fitness beginners)
* Messaging like: productivity + health optimization
* Ad copies for Twitter, Instagram, and headlines
* Visual ideas like app UI mockups, fitness tracking dashboards
* Final structured campaign brief

---

## 📌 Key Strengths of This Project

* Real multi-agent pipeline (not single prompt engineering)
* Clear separation of responsibilities across agents
* State-driven communication between agents
* Extensible architecture (easy to add new agents)
* Real-world marketing automation use case

---

## ⚠️ Note

This module was originally part of a larger ADK-based system and has been isolated for demonstration and portfolio purposes.

---

## 👨‍💻 Author

Built as an AI agent system exploring real-world marketing automation using multi-agent LLM orchestration.
