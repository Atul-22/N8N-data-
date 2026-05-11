# ⚙️ n8n AI Automation Workflows

[![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-orange?style=flat-square)](https://n8n.io)
[![Gemini](https://img.shields.io/badge/Google-Gemini%202.5%20Flash-blue?style=flat-square&logo=google)](https://ai.google.dev)
[![GitHub](https://img.shields.io/badge/GitHub-Atul--22-black?style=flat-square&logo=github)](https://github.com/Atul-22)

> A collection of production-ready AI automation workflows built with n8n and Google Gemini API. Each workflow demonstrates real-world agentic AI thinking — from multi-agent orchestration to AI evaluation frameworks.

---

## 🚀 Workflows

---

### 1. 🧠 AI Product Ideation & Prioritization Pipeline

A **5-agent sequential pipeline** that takes a raw product idea from Google Sheets and produces a full executive-ready analysis automatically.

**Agent Flow:**
```
Google Sheets Trigger (new row added)
  → Ideation Agent         — refines idea, generates alternatives, scores innovation
  → Market Research Agent  — TAM/SAM sizing, competitor analysis, market trends
  → Prioritization Agent   — RICE/ICE scoring, priority tier (High/Medium/Low)
  → Roadmap Agent          — MVP features, Phase 2 & 3 planning, team requirements
  → Executive Summary Agent — final Go/No-Go recommendation
  → Google Sheets Output   — writes 40+ fields back to Output Sheet
  → Gmail                  — sends executive summary to email
```

**Tech Stack:** n8n · Gemini 2.5 Flash Lite · Google Sheets API · Gmail API · JavaScript

**Key Features:**
- Fully automated end-to-end product analysis triggered by a spreadsheet row
- Each agent outputs structured JSON validated by custom JavaScript code nodes
- Outputs 40+ data fields including priority score, ICE score, roadmap phases, risk mitigation plan
- Results written back to Google Sheets and emailed automatically

---

### 2. 🔬 PhD Research Assistant (3-Agent System)

A **3-agent parallel research system** exposed as a REST API, with JWT authentication and webhook routing.

**Architecture:**
```
Webhook (POST /api)
  → Router (path detection: login / signup / research)
  → Is Login?  → Handle Login  → Respond
  → Is Signup? → Handle Signup → Respond
  → Orchestrator
      ├── Research Scout Agent   — literature landscape, research gaps, methodology trends
      ├── Topic Advisor Agent    — 3-5 refined topics with feasibility scores (1-10)
      └── AI Assistant Agent    — career relevance, impact potential, honest cautions
  → Merge & Format Output → Respond to Webhook (JSON)
```

**Tech Stack:** n8n · Gemini 2.5 Flash (3 instances) · Webhook API · JavaScript

**Key Features:**
- JWT-based login and signup authentication built entirely in n8n
- 3 specialized agents run in parallel for faster, richer output
- Structured JSON response merging all 3 agent outputs
- Integrated with Lovable frontend via CORS-enabled webhook

---

### 3. 📈 Stock Market Analyzer

A **chat-triggered stock analysis agent** that generates professional buy/hold/sell recommendations and emails the full report.

**Flow:**
```
Chat Trigger (user types a stock ticker)
  → AI Agent (Gemini 2.5 Flash + Simple Memory)
      — Technical analysis: trend, support/resistance, moving averages, volume
      — Fundamentals: P/E ratio, earnings trends, competitive position
      — Recommendation: BUY / HOLD / SELL with confidence level
      — Price target, stop loss, time horizon, key risks
  → Gmail (auto-emails the formatted report)
```

**Tech Stack:** n8n · Gemini 2.5 Flash Lite · Simple Memory Buffer · Gmail API

**Key Features:**
- Conversational interface — just type any stock ticker symbol
- Memory buffer maintains context across the conversation
- Structured 300-word professional report format
- Auto-emails the analysis after every query

---

### 4. 🌍 AI Travel Planner

A **webhook-based travel itinerary generator** that creates personalized day-by-day travel plans via REST API.

**Flow:**
```
Webhook (POST /travel-itinerary)
  Accepts: location, travel dates, travel type
  → AI Agent (Gemini)
      — Day-by-day schedule: morning, afternoon, evening activities
      — Restaurant recommendations with cuisine types
      — Must-see attractions with descriptions
      — Practical tips and estimated costs
  → Respond to Webhook (JSON)
```

**Tech Stack:** n8n · Gemini Chat Model · Webhook API

**Key Features:**
- REST API endpoint — integrable with any frontend
- Personalized output based on travel type (solo, family, business, adventure)
- Clean structured JSON response

---

### 5. 🛒 Amazon Customer Support Evaluator

An **AI agent evaluation framework** that tests and scores an Amazon customer support bot using n8n's native evaluation system.

**Flow:**
```
Evaluation Trigger (fetches test cases from Google Sheets dataset)
  → AI Agent (acts as Amazon support agent)
      — Handles: order issues, returns, delivery queries
      — Rules: polite, no policy fabrication, asks clarification if needed
  → Evaluation (checkIfEvaluating)
  → Evaluation1 (setOutputs — logs AI response per test case)
  → Evaluation2 (setMetrics — scores is_polite: 1 if polite, 0 if not)
```

**Tech Stack:** n8n · Gemini Chat Model · Google Sheets · n8n Evaluation Framework

**Key Features:**
- Uses n8n's native evaluation framework for systematic AI quality testing
- Custom metric: `is_polite` — detects empathy keywords (thank, sorry, help, assist)
- Dataset-driven testing from Google Sheets for repeatable evals
- Shows AI product thinking: build → test → measure → iterate

---

## 🛠️ Tech Stack

![n8n](https://img.shields.io/badge/n8n-Automation-orange?style=flat-square)
![Gemini](https://img.shields.io/badge/Gemini-2.5%20Flash-blue?style=flat-square&logo=google)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Integration-green?style=flat-square&logo=googlesheets)
![Gmail](https://img.shields.io/badge/Gmail-API-red?style=flat-square&logo=gmail)
![JavaScript](https://img.shields.io/badge/JavaScript-Code%20Nodes-yellow?style=flat-square&logo=javascript)
![Webhook](https://img.shields.io/badge/Webhook-REST%20API-purple?style=flat-square)

---

## 💡 Why I Built This

As an AI-native Product Manager, I believe in building what I ship. These workflows demonstrate:

- **Agentic AI thinking** — decomposing complex tasks into specialized agents with clear roles
- **Real-world use cases** — not toy examples, but production-relevant automations
- **End-to-end ownership** — from ideation to working, tested automation
- **AI evaluation mindset** — building metrics to measure and improve AI output quality

---

## 📬 Connect

- 💼 [LinkedIn](https://www.linkedin.com/in/atul-pandey-98962722b)
- 🐙 [GitHub](https://github.com/Atul-22)
- 🤗 [Hugging Face](https://huggingface.co/Atul0422)

---

<div align="center">
  <i>Built by Atul Pandey — AI Product Manager | Open to APM roles in India 🇮🇳</i>
</div>
