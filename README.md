# n8n Automations

A curated collection of production-ready AI agentic systems and workflow automations built using **n8n**, **Groq LPU (Llama 3.3 70B)**, **LangChain**, **Gmail API**, **Google Sheets**, and **SerpApi**.

Each project in this repository includes fully functional workflow JSON definitions, interactive web dashboards / client portals, visual canvas screenshots, and comprehensive technical documentation.

---

## Automation Portfolio

| Automation | Description | Core Tech Stack | Documentation & Assets |
| :--- | :--- | :--- | :---: |
| **[Autonomous Sales Machine](./Autonomous%20Sales%20Machine)** | Autonomous B2B sales engine that evaluates incoming leads (1–10 score), writes personalized 3-paragraph cold emails, delivers via Gmail, monitors inbox replies, and schedules 2-day follow-ups with live client & analytics dashboards. | `n8n` · `Groq Llama 3.3 70B` · `Gmail API` · `Google Sheets` · `Chart.js` | [Explore System](./Autonomous%20Sales%20Machine/README.md) |
| **[Groqtalk AI](./Groqtalk%20AI)** | Multi-agent reasoning and critic system with an automated self-evaluation feedback loop and real-time Google Search fallback via SerpApi, accompanied by a dark-mode chat UI. | `n8n` · `Groq Llama 3.3 70B` · `SerpApi` · `TailwindCSS` · `JavaScript` | [Explore System](./Groqtalk%20AI/README.md) |
| **[SmartPost AI](./SmartPost%20AI)** | Multi-channel social media repurposing engine that transforms a single core concept into tailored LinkedIn posts, Twitter threads, Instagram captions, and SEO blog outlines with Google Sheets CRM logging. | `n8n` · `Groq Llama 3.3 70B` · `Google Sheets` · `TailwindCSS` · `JavaScript` | [Explore System](./SmartPost%20AI/README.md) |

---

## Repository Structure

```text
n8n-automations/
├── Autonomous Sales Machine/
│   ├── README.md                                      # Comprehensive workflow documentation
│   ├── Autonomous Sales Machine.json                  # Complete 31-node n8n workflow definition
│   ├── Autonomous Sales Machine Workflow screenshot.png # High-resolution workflow canvas
│   ├── Autonomous Sales Machine Dashboard.jpeg        # Live analytics dashboard preview
│   ├── Aut Sales Machine Client Portal.jpeg           # Client portal interface preview
│   ├── Dashboard.html                                 # Interactive KPI & analytics dashboard
│   └── Client Portal.html                             # Multi-client authenticated dashboard
│
├── Groqtalk AI/
│   ├── README.md                                      # Multi-agent architecture documentation
│   ├── Groq Multi-Agent Lite.json                     # 10-node reasoning & critic workflow definition
│   ├── Groqtalk workflow screenshot.png               # Workflow canvas screenshot
│   ├── Groqtalk dashboard.jpeg                        # Chat interface preview
│   ├── Groqtalk Welcome screen.jpeg                   # Onboarding screen preview
│   └── GROQTALK PRO.html                              # Standalone web chat client
│
└── SmartPost AI/
    ├── README.md                                      # Content engine documentation
    ├── SmartPost Ai.json                              # 9-node parallel generation workflow definition
    ├── Smart post ai workflow screnshot.png           # Workflow canvas screenshot
    ├── smartpost ai dashboard.jpeg                    # Content studio preview
    └── SmartPost AI.html                              # Multi-format generator web UI
```

---

## Interactive Dashboards & Web Portals

All included HTML applications are self-contained, standalone web interfaces that can be run directly in any modern browser to demonstrate the frontend layer of each automation:

- **Autonomous Sales Machine**:
  - [Executive Dashboard (Local)](./Autonomous%20Sales%20Machine/Dashboard.html) · 🌐 **[Live Hosted Dashboard](https://ehtishamazing.github.io/sales-dashboard/index.html)** — Real-time campaign tracking, pipeline status charts, and lead score distribution.
  - [Client Portal](./Autonomous%20Sales%20Machine/Client%20Portal.html) — Client-accessible portal with credential gating and campaign visibility.
- **Groqtalk AI**:
  - [GROQTALK PRO](./Groqtalk%20AI/GROQTALK%20PRO.html) — Modern AI chat application with multi-chat persistence in local storage.
- **SmartPost AI**:
  - [SmartPost Studio](./SmartPost%20AI/SmartPost%20AI.html) — 4-in-1 content generator studio with brand voice controls and generation history.

---

## Tech Stack Overview

- **Orchestration**: [n8n](https://n8n.io/) (Workflow Automation)
- **AI Models & Acceleration**: [Groq Cloud](https://groq.com/) with `llama-3.3-70b-versatile`
- **Agentic Frameworks**: `@n8n/n8n-nodes-langchain` LLM chains & chat model interfaces
- **Cloud Integrations**: Google Sheets OAuth2 API, Gmail OAuth2 API, SerpApi
- **Frontend Technologies**: HTML5, Vanilla JavaScript, TailwindCSS, Chart.js, FontAwesome

---

## Setup & Importing Workflows

1. **Clone the Repository**:
   ```bash
   git clone <REPOSITORY_URL>
   cd n8n-automations
   ```
2. **Import Workflow into n8n**:
   - Open your n8n web interface.
   - Go to **Workflows** → **Import from File**.
   - Select the desired `.json` file from any automation directory.
3. **Configure Environment & Credentials**:
   - **Groq API**: Add your API key in the respective HTTP Request or LangChain Groq Chat Model nodes.
   - **Google Sheets & Gmail**: Authenticate via your Google OAuth2 credentials in n8n.
   - **SerpApi**: Set your SerpApi key for real-time web search nodes.
4. **Activate**: Set the workflow to **Active** to start listening for webhook events or scheduled cron triggers.

---

## Demo Videos

Full walkthroughs and live execution demonstrations are published on LinkedIn:

- **Autonomous Sales Machine Demo**: `LinkedIn Demo: TO_BE_ADDED`
- **Groqtalk AI Demo**: `LinkedIn Demo: TO_BE_ADDED`
- **SmartPost AI Demo**: `LinkedIn Demo: TO_BE_ADDED`

---

## Security & Best Practices

- All API keys, access tokens, and sensitive private credentials have been stripped from the exported JSON workflow files.
- Placeholders such as `YOUR_GROQ_API_KEY` and `YOUR_SERPAPI_KEY` are used to indicate where users should attach their own credentials.
