# n8n Automation Portfolio

A collection of production-ready n8n workflows built for small and mid-size service businesses. Each workflow is plug-and-play — swap in credentials and go live.

---

## Workflows

### AI & Lead Generation
| Workflow | Trigger | What it does |
|---|---|---|
| [Speed-to-Lead AI Responder](./workflows/speed-to-lead-ai-responder.json) | Webhook | GPT reads a new lead's message and sends a personalized reply within 60 seconds. Owner gets an instant alert. |
| [AI Outreach Agent](./workflows/ai-outreach-agent.json) | Manual | Reads a lead list from Google Sheets, writes personalized cold emails with GPT, sends and logs everything. |
| [AI Customer Support Auto-Reply](./workflows/ai-customer-support-auto-reply.json) | Gmail Trigger | Triages every support email — auto-replies to FAQ questions, escalates complex ones to a human with AI notes. |

### Customer Retention & Reviews
| Workflow | Trigger | What it does |
|---|---|---|
| [HVAC Post-Job Review Request](./workflows/hvac-post-job-review-request.json) | Webhook | Sends a review request 2 hours post-job, then a smart follow-up at 48 hours. Emergency jobs get a maintenance plan offer. |
| [Google Review Monitor & AI Responder](./workflows/google-review-monitor-ai-responder.json) | Schedule (2hr) | Monitors Google Business reviews, writes personalized AI responses (warm for 4-5 stars, empathetic for 1-3), and auto-posts. |
| [Quote & Estimate Follow-Up Sequence](./workflows/quote-estimate-followup-sequence.json) | Webhook | 3-touch follow-up over 7 days on unsent quotes: check-in → value-add → urgency close. |

### Scheduling & Appointments
| Workflow | Trigger | What it does |
|---|---|---|
| [Appointment Reminder Sequence](./workflows/appointment-reminder-sequence.json) | Webhook | Sends booking confirmation instantly, then timed reminders at exactly 24hr and 2hr before the appointment. |

### Social Media
| Workflow | Trigger | What it does |
|---|---|---|
| [Instagram Content Generator](./workflows/instagram-content-generator.json) | Schedule (weekly) | GPT generates 7 posts every Monday, queues them in Google Sheets, and emails a Canva image checklist. |
| [Instagram Auto-Poster](./workflows/instagram-auto-poster.json) | Schedule (daily) | Checks the content queue each morning and publishes scheduled posts to Instagram via Meta Graph API. |

---

## Stack

- **Platform:** [n8n](https://n8n.io) (cloud-hosted)
- **AI:** OpenAI GPT (via n8n LangChain nodes)
- **Integrations:** Gmail, Google Sheets, Instagram Graph API, Google Business Profile, webhooks

---

## Usage

Each `.json` file in `/workflows` contains the node structure and logic for that workflow. To use one:

1. Import the JSON into your n8n instance
2. Add your credentials (Gmail OAuth2, OpenAI API key, etc.)
3. Replace any placeholder values (marked `PASTE_...`)
4. Activate

---

Built by Cael Garriott | [Qalam Automation](https://qalamdesigns.com)
