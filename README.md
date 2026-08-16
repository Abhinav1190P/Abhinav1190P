<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg">
  <img alt="Abhinav Pandey — Full-Stack Software Engineer, Agentic AI & RAG Systems" src="./assets/banner-dark.svg" width="100%">
</picture>

<br/>

<p>
<a href="https://latest-portfolio-z2oy.onrender.com"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-0b0f19?style=flat-square&logo=googlechrome&logoColor=22d3ee"/></a>
<a href="https://leetcode.com/u/abhinvnarc"><img alt="LeetCode" src="https://img.shields.io/badge/LeetCode-0b0f19?style=flat-square&logo=leetcode&logoColor=FFA116"/></a>
<a href="https://www.linkedin.com/in/abhinav-pandey-432b62226/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0b0f19?style=flat-square&logo=linkedin&logoColor=22d3ee"/></a>
<a href="mailto:pandeysandeep1190@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-0b0f19?style=flat-square&logo=gmail&logoColor=a78bfa"/></a>
<img alt="Profile views" src="https://komarev.com/ghpvc/?username=Abhinav1190P&style=flat-square&color=0b0f19&label=views"/>
</p>

## At a glance

| Manual turnaround | Page load | Table scale | Dashboard reach | Defects closed | RAG accuracy |
|:--:|:--:|:--:|:--:|:--:|:--:|
| ↓ 20% | ↓ 25–30% | 5,000+ rows/table | 50+ users · 6+ teams | 40+ resolved | 85% → 92% |

<sup>Metrics from production work at IQVIA (agentic AI for ROM/estimation) and DocMind's 13-question retrieval eval harness.</sup>

## Toolbox

```
frontend    react · redux-saga · mui data grid · react router
backend     node.js · express · .net 8 · fastapi
agentic-ai  langchain · tool-calling agents · vector re-ranking · groq/llama
data        mongodb · atlas vector search · sql server
cloud       aws (ec2 · s3 · lambda · iam · cloudwatch) · docker · firebase
quality     jwt/oidc · swagger/openapi · jest · gitlab api v4 ci/cd
```

## Experience

| | | |
|:--|:--|:--|
| **12/2024 → Present** | **Software Engineer**, IQVIA India | Agentic AI for ROM estimation & capacity forecasting (8+ projects) · pagination for 10+ tables at 5,000+ rows · KPI dashboards for 50+ users · .NET 8 microservices with JWT/OIDC |
| **12/2023 → 02/2024** | Full Stack Dev Intern, Krunk.AI | Bootstrapped a React app end-to-end; Firebase auth across 8+ modules |
| **11/2022 → 01/2023** | Chrome Ext. Dev Intern, ClickUp | "To-Doist for ClickUp" — 50+ pilot testers |
| **2024** | B.E., Mumbai University | — |

<br/>

<img src="./assets/header-projects.svg" width="100%" alt="Featured Projects"/>

<br/>

### 🧠 [DocMind — Agentic RAG Document Assistant](https://docmind-client-bdfn.onrender.com)
`react` `node/express` `python · fastapi` `langchain` `mongodb atlas`

A tool-calling RAG agent that grounds itself in your documents first, and only reaches for outside help when it has to.

```mermaid
flowchart LR
    U([User Query]) --> A{Agent Loop}
    A -- "1: retrieve" --> D[(MongoDB Atlas<br/>Vector Search)]
    D -- "re-ranked context<br/>cross-encoder" --> A
    A -- "2: fallback" --> W[[Web Search<br/>Tavily]]
    A -- "3: fallback" --> C[[Sandboxed<br/>Calculator]]
    W --> A
    C --> A
    A --> G([Groq / Llama<br/>Generation])
    G --> R([Grounded Answer<br/>+ Citations + Trace])

    style A fill:#04241c,stroke:#00e676,color:#f4f6fb
    style G fill:#04241c,stroke:#00c9a7,color:#f4f6fb
    style R fill:#04241c,stroke:#00e676,color:#f4f6fb
```

- Cross-encoder re-ranking on retrieval lifted answer accuracy **85% → 92%** on a 13-question evaluation harness built to score retrieval + generation quality
- Full execution trace — which tool fired, why, with what result — surfaced in the UI, not buried in logs
- Diagnosed and resolved production issues (memory limits, rate limiting, Docker) across three independently deployed services on Render

### 🛒 Subs4Sale — Freelancer Marketplace
`react` `node.js` `express` `mongodb` `socket.io`

A Fiverr-style freelancer–client marketplace built solo, end to end — listings, real-time chat, transactions, and reviews on one MERN codebase.

```mermaid
flowchart LR
    subgraph Client["React Frontend"]
        UI[Browse / Gig Listings]
        ChatUI[Real-time Chat]
        AuthUI[Sign Up / Login]
    end

    subgraph Server["Node.js + Express API"]
        AuthSvc[Auth Service]
        ListingSvc[Listings API]
        TxnSvc[Transactions API]
        ReviewSvc[Ratings & Reviews API]
        Socket[[Socket Layer]]
    end

    DB[(MongoDB)]

    AuthUI --> AuthSvc --> DB
    UI --> ListingSvc --> DB
    UI --> TxnSvc --> DB
    UI --> ReviewSvc --> DB
    ChatUI <--> Socket --> DB

    style Server fill:#04241c,stroke:#00e676,color:#f4f6fb
    style DB fill:#04241c,stroke:#00c9a7,color:#f4f6fb
```

- Designed the full MongoDB schema architecture from scratch — users, gigs, transactions, and reviews as independently queryable collections
- Built secure authentication, a real-time chat layer, and end-to-end transaction workflows (request → accept → pay → review)
- React.js frontend consuming a self-built Node.js/Express REST API; published and documented on GitHub for others to reference

<br/>

<img src="./assets/header-leetcode.svg" width="100%" alt="LeetCode"/>

<br/>

<p align="center">
<img src="https://leetcard.jacoblin.cool/abhinvnarc?theme=light&font=Karma&ext=heatmap" width="90%" alt="LeetCode stats"/>
</p>

<p align="center">
<a href="https://leetcode.com/u/abhinvnarc"><img alt="Solve with me on LeetCode" src="https://img.shields.io/badge/View%20full%20profile%20on%20LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black"/></a>
</p>

<br/>

<img src="./assets/header-accomplishments.svg" width="100%" alt="Accomplishments"/>

<br/>

<table width="100%">
<tr>
<td width="50%" valign="top">

#### 🥇 Smart India Hackathon 2022 — Winner
**AICTE Grievance Management Portal**

A time-bound, automated resolution workflow for student grievances — recognized as the winning solution among **200+ competing teams** nationwide.

</td>
<td width="50%" valign="top">

#### 🥈 Tantrotsav Hackathon — First Runner-Up
**MERN Social Media App**

Secure authentication, real-time messaging, and Cloudinary/Zeegocloud integration, built under hackathon time pressure.

</td>
</tr>
</table>

<p align="center">
<img src="./assets/sih-2022-winners.jpg" width="85%" alt="Team with the winning cheque on stage at the Smart India Hackathon 2022 Grand Finale"/>
<br/>
<sub>🏆 On stage at the SIH 2022 Grand Finale, Software Edition — team win, ₹1,00,000 prize</sub>
</p>

<br/>

## Live stats

<details>
<summary><b>GitHub metrics</b> (auto-refreshes every 6h via <code>.github/workflows/metrics.yml</code>)</summary>
<br/>

<img src="https://raw.githubusercontent.com/Abhinav1190P/Abhinav1190P/main/metrics.svg" width="100%" alt="metrics"/>

<sub>Requires enabling the included <code>lowlighter/metrics</code> workflow and adding a <code>METRICS_TOKEN</code> secret (a classic PAT with <code>repo</code> + <code>read:user</code>) — see setup notes below.</sub>

</details>

<p align="center">
<img src="https://github-readme-stats.vercel.app/api?username=Abhinav1190P&show_icons=true&hide_border=true&theme=default&text_color=1c2333&title_color=0891b2&icon_color=7c3aed" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Abhinav1190P&layout=compact&hide_border=true&theme=default&text_color=1c2333&title_color=0891b2&langs_count=8" height="165"/>
</p>

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Abhinav1190P/Abhinav1190P/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Abhinav1190P/Abhinav1190P/output/github-contribution-grid-snake.svg">
  <img alt="contribution snake" src="https://raw.githubusercontent.com/Abhinav1190P/Abhinav1190P/output/github-contribution-grid-snake.svg" width="100%"/>
</picture>
<sub>Generated by <code>.github/workflows/snake.yml</code> on push to <code>output</code></sub>
</p>

---

> **Setup notes for the dynamic pieces:** this repo ships `.github/workflows/metrics.yml` and `.github/workflows/snake.yml`. Enable Actions on the repo, add a `METRICS_TOKEN` secret for the metrics workflow (Settings → Secrets → Actions), and both will start committing fresh SVGs on their schedule — the embeds above will pick them up automatically once they exist.
