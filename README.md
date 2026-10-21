# 🗼 AI Watch Tower

**A real-time AI governance control plane that sits between employees and Generative AI, detecting shadow AI usage, masking sensitive data, scoring risk, and producing audit-ready compliance trails.**

> Team **AURAX** · PSID 006 · Jain (Deemed-to-be) University, Bengaluru
> Submission for **CXO InnoFest 2025**

---

## 📌 Overview

Employees increasingly paste company data into ChatGPT, Gemini, Claude and other GenAI tools, often without approval ("shadow AI"). This leads to leaked PII, exposed source code, hallucinated outputs being trusted blindly, and no audit trail for regulators.

**AI Watch Tower** intercepts every prompt *before* it reaches the model, evaluates it, and enforces a tiered, human-in-the-loop response, not just detection.

## ✨ Key Features

| Feature | What it does |
|---|---|
| **Inline Interception** | Real-time control layer between employees and GenAI tools |
| **Dynamic Risk Scoring** | Scores every session using behavioral telemetry and task sensitivity (Roverreliance™) |
| **Real-Time Data Masking** | Detects and redacts Aadhaar, PAN, passwords and IP before prompts reach the model |
| **Tiered Intentional Friction** | Confidence heatmaps and copy-paste limits force human verification on risky outputs |
| **Continuous Compliance Audit** | Every interaction mapped to NIST AI RMF and ISO/IEC 42001-ready audit trails |
| **Policy-as-Code** | Compliance teams update guardrails dynamically, with no core code changes |

### Risk-tiered enforcement

```
Employee Prompt
      │
      ▼
 AI WATCH TOWER  ── PII detection · Dynamic risk scoring
      │
      ├── LOW RISK    → ALLOW
      ├── MEDIUM RISK → WARN & PROCEED
      └── HIGH RISK   → HUMAN REVIEW
      │
      ▼
 Audit log & compliance (NIST AI RMF · ISO/IEC 42001)
```

## 🏭 Use Cases

- **IT & Software:** blocks hallucinated code and shadow-AI data leaks
- **Banking & Financial Services:** masks PAN, Aadhaar and account numbers in real time
- **Healthcare:** forces manual verification of AI-generated diagnostics
- **Legal & Compliance:** auto-generates NIST AI RMF and ISO/IEC 42001 audit logs
- **Human Resources:** prevents PII leaks and enforces human-in-the-loop checks
- **Government & Public Sector:** intercepts malicious prompts and hallucinated policy outputs

## 🧱 Tech Stack

**Current repository (frontend starter)**

- React 18 + React Router 6
- Vite 5
- Tailwind CSS 3

**Planned architecture**

| Layer | Technology |
|---|---|
| Frontend | React.js, HTML/CSS/JS |
| Backend | Python, FastAPI, Vanta API |
| AI & NLP | Microsoft Presidio, spaCy, CES + Linear Probes |
| Risk Engine | Openlayer (Roverreliance™) |
| Database | MongoDB / PostgreSQL |
| Dashboard | Chart.js / Streamlit |

## 🚦 Project Status

This repository currently contains the **frontend starter**. Data on screen is **mocked**, and backend calls are marked with `TODO` comments in the code.

| Screen | Route | Status |
|---|---|---|
| Login | `/login` | ✅ UI built (mock auth) |
| Dashboard | `/dashboard` | ✅ UI built (mock data) |
| AI Prompt | `/prompt` | ✅ UI built (mock submit) |
| Prompt Analysis | `/analysis` | ✅ UI built (mock PII and policy results) |
| AI Response | `/response` | 🚧 Placeholder |
| Approval Queue | `/approval` | 🚧 Placeholder |
| Analytics | `/analytics` | 🚧 Placeholder |
| Reports | `/reports` | 🚧 Placeholder |
| Policy Management | `/policy` | 🚧 Placeholder |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 18 or later
- npm (bundled with Node.js)

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>/aiwatchtower

# Install dependencies
npm install

# Start the dev server
npm run dev
```

The app runs at **http://localhost:5173**. Sign in with any email and password (authentication is mocked for now).

### Available scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the Vite dev server |
| `npm run build` | Create a production build in `dist/` |
| `npm run preview` | Preview the production build locally |

## 📁 Project Structure

```
aiwatchtower/
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
└── src/
    ├── main.jsx              # App entry + route definitions
    ├── index.css             # Tailwind + global styles
    ├── components/
    │   ├── Sidebar.jsx
    │   ├── Topbar.jsx
    │   └── StatCard.jsx
    └── pages/
        ├── Login.jsx
        ├── Dashboard.jsx
        ├── PromptPage.jsx
        └── AnalysisPage.jsx
```

## 🗓️ Roadmap (6-week plan)

| Week | Milestone |
|---|---|
| 1 | Requirement analysis & planning |
| 2 | UI/UX design |
| 3 | Backend & database development |
| 4 | AI integration & policy engine |
| 5 | Testing & bug fixes |
| 6 | Deployment & final documentation |

**Next up:** FastAPI auth and prompt-interception endpoints, Presidio PII scanning, the Policy-as-Code engine, the Approval Queue, and audit-log export.

## ⚠️ Known Challenges

- False positives and negatives in sensitive-data detection
- Hallucinations may still require manual verification
- Integration with existing enterprise platforms
- Compliance requirements vary across industries and countries
- High request volumes need scalable cloud infrastructure

## 🔭 Future Enhancements

- **Advanced threat intelligence:** coverage for the OWASP Top 10 for LLMs (prompt injection, model poisoning, phantom squatting) and "vibe coding" risks in CI/CD
- **LLMOps & FinOps guardrails:** LLM-as-a-Judge semantic evaluation, agent RBAC and token rate-limiting
- **HCI psychology:** cognitive forcing functions (confirmation checkpoints, confidence heatmaps) to counter automation bias and vigilance decay

## 👥 Team AURAX

| Name | Role |
|---|---|
| Pranitha Pramod | Team Leader / AI-NLP Engineer |
| Amina Zera Rahees | Full Stack |
| Anujaya Bijay | Backend / Security Developer (Python, FastAPI) |
| Nandana D Nair | Frontend Developer (React.js) |

**Mentors:** Dr. Garima Sinha and Priya Chanda

**Institution:** Jain (Deemed-to-be) University, Bengaluru

## 📄 License

Add a license of your choice (for example MIT) before publishing.
