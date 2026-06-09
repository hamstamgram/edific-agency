# Edific

**AI Automation Agency — Building Smarter Systems for Growing Businesses**

🌐 **Website:** [edific.uk](https://edific.uk)

---

## About Edific

Edific is an AI automation agency that helps businesses streamline operations, capture more leads, and deliver exceptional customer experiences through intelligent automation. We build the systems that let you focus on growing your business.

We specialize in **med spas, dental practices, and home service companies** — industries where every missed call or slow follow-up costs real revenue.

---

## Services

### 🤖 AI Chatbots (Claude-Powered)
Intelligent conversational agents that handle customer inquiries 24/7 — qualifying leads, booking appointments, and answering FAQs without human intervention.

- Website chat widgets
- SMS/MMS conversational bots
- Lead qualification and scoring
- Multi-turn dialogue management
- Custom knowledge base integration

### ⚙️ n8n Workflow Automation
Custom workflows that connect your tools and automate repetitive tasks — from lead routing to appointment scheduling to post-service follow-ups.

- CRM integrations (GoHighLevel, HubSpot, Salesforce)
- Calendar and booking automation
- Data synchronization between platforms
- Custom API integrations
- Webhook-based event triggers

### 📞 Voice AI Agents (Vapi / Retell)
AI-powered phone agents that answer calls, schedule appointments, and follow up with prospects — handling the calls your team cannot get to.

- Inbound call handling and triage
- Outbound appointment confirmation
- Missed call recovery campaigns
- Voicemail drop and callback scheduling
- Real-time transcript and summary dashboards

### 🎯 Lead Generation Systems
End-to-end lead capture and nurturing pipelines that turn strangers into booked appointments.

- Facebook/Google Ads to CRM automation
- Landing page to follow-up sequences
- Review request automation
- Referral program systems
- Re-engagement campaigns for dormant leads

---

## Tech Stack

| Category | Tools |
|----------|-------|
| **Workflow Engine** | n8n (self-hosted and cloud) |
| **AI / LLM** | Claude (Anthropic), OpenAI GPT-4 |
| **Voice** | Vapi, Retell AI |
| **CRM / Marketing** | GoHighLevel, HubSpot, ActiveCampaign |
| **Databases** | PostgreSQL, Supabase, Airtable |
| **Hosting** | Railway, Render, AWS, VPS |
| **Communication** | Twilio, SendGrid, Postmark |
| **Monitoring** | Grafana, Uptime Robot, custom dashboards |

---

## Pricing

| Tier | Price | What's Included |
|------|-------|-----------------|
| **Quick Gig** | €199 – €999 setup | Single workflow, chatbot setup, or one-off automation |
| **Hourly** | €95/hr | Custom development, consulting, debugging |
| **Retainer** | €1,500/mo | Ongoing support, monthly optimization, priority response |

Custom packages available for enterprise clients.

---

## Getting Started

1. **Book a call** — Tell us about your business and pain points
2. **Audit and proposal** — We map your workflows and recommend automations
3. **Build and test** — We develop, sandbox test, and refine
4. **Launch and monitor** — Go live with monitoring and support

---

## Repository Structure

```
edific/
├── workflows/          # n8n workflow exports and templates
├── demos/              # Demo scripts, screenshots, video links
├── docs/               # Setup guides, architecture docs, SOPs
├── templates/          # Reusable templates and boilerplates
├── screenshots/        # Portfolio images and workflow screenshots
├── index.html          # Landing page (GitHub Pages)
├── CNAME               # Custom domain for GitHub Pages
├── README.md           # This file
├── LICENSE             # MIT License
└── .gitignore          # Standard ignores
```

---

## GitHub Pages Deployment

This repo is deployed as a static site at [edific.uk](https://edific.uk) using GitHub Pages.

### Setup Instructions

1. **Push your landing page** — The `index.html` file in the repo root is served as the site homepage.

2. **Add a CNAME file** — A `CNAME` file is included with the content `edific.uk` to configure the custom domain.

3. **Configure GitHub Pages:**
   - Go to **Settings → Pages** in the GitHub repo
   - Under **Source**, select **Deploy from a branch**
   - Choose the `main` branch and `/ (root)` folder
   - Click **Save**

4. **Set up your domain DNS:**
   - Add an **A record** pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Or add a **CNAME record** pointing to `hamstamgram.github.io`
   - Enable **Enforce HTTPS** in the Pages settings once DNS propagates

5. **Verify** — Visit [https://edific.uk](https://edific.uk) to confirm the site is live.

> **Note:** DNS propagation can take up to 24–48 hours. GitHub Pages provides free SSL certificates automatically.

---

## Workflows

Check out the `workflows/` directory for example n8n workflow exports you can import directly into your n8n instance.

---

## Portfolio

Visit `demos/` for walkthroughs, screenshots, and case studies of automations we have built.

---

## Documentation

Setup guides, architecture decisions, and standard operating procedures live in `docs/`.

---

## Contact

- **Website:** [edific.uk](https://edific.uk)
- **GitHub:** [hamstamgram](https://github.com/hamstamgram)
- **Email:** hello@edific.uk

---

## License

This repository and its contents are licensed under the MIT License — see LICENSE for details.

---

*Built with care by Edific — Automate. Accelerate. Scale.*
