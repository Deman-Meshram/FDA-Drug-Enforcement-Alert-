# FDA Drug Enforcement Alert — Pharma Compliance Monitor

> Real-time FDA drug recall and enforcement monitoring for Pharma professionals.



![Status](https://img.shields.io/badge/Status-Complete-brightgreen)



---

## What It Does

Automatically fetches latest FDA drug enforcement actions, generates AI summaries, and delivers formatted email alerts.

- **Real-time FDA monitoring** — fetches latest drug recalls and enforcement actions
- **AI summaries** — Groq generates concise summary per recall
- **Google search links** — direct search links per recall for deep research
- **Gmail alerts** — formatted HTML email with all details
- **Scheduled automation** — runs automatically, no manual trigger needed

---

## Tech Stack

| Layer | Tool |
|---|---|
| Automation | n8n workflow |
| Data API | openFDA API |
| LLM | Groq (llama-3.1-8b) |
| Email | Gmail HTML |

---

## Architecture

```
Scheduled trigger (n8n)
        ↓
openFDA API fetches latest enforcement actions
        ↓
Groq AI generates summary per recall
        ↓
Google search links added per recall
        ↓
Gmail sends formatted HTML alert
```

---

## Key Features

- Automated FDA enforcement action monitoring
- AI-generated recall summaries
- Google search links per recall
- HTML formatted Gmail alerts
- Date parsing from raw FDA format (YYYYMMDD)

---

## Technical Notes

- openFDA API used for drug enforcement endpoint
- Date format converted from raw `20260527` via substring parsing
- Google search links used instead of FDA deep links (unreliable)
- Groq llama-3.1-8b used for fast, reliable summarization
- Summary path: `item.json.output`

---

*Built by Deman Meshram | BSc Biotechnology + AI Automation*
