# Awesome-Marketing-Automation-Lead-Nurturing

# Awesome Marketing Automation & Lead Nurturing

> A curated list of top Marketing Automation and Lead Nurturing platforms — both SaaS/Hosted commercial solutions and open-source alternatives for capturing leads, scoring engagement, and automating personalized follow-up sequences.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
- [Open-Source Software](#-open-source-software)
  - [Mautic](#mautic)
  - [Helio](#helio)
  - [NocoCRM](#nococrm)
  - [Sphericon](#sphericon)
  - [OpenLeads](#openleads)
  - [entirius-django-leads](#entirius-django-leads)
  - [erxes](#erxes)

---

## 📊 Sector Overview & Market Dynamics

The global marketing automation software market was estimated at approximately **$5.1B to $6.7B in 2024** (growing at an 11–15% CAGR toward **$6.2B–$8.4B+**). The sector is **moderately fragmented**: it displays a top-heavy concentration where a handful of enterprise CRM and marketing giants (Salesforce, Adobe, HubSpot) hold nearly 45–50% of revenue, while hundreds of specialized, mid-market, and open-source point solutions actively compete in a fragmented long tail.

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Marketing Automation and Lead Nurturing platforms. These are not open-source but are included as reference points for feature comparison. Sorted descending by company size (valuation / revenue).

| Platform | Parent / Company Size (Revenue / Valuation) | Starting Pricing | Free Tier / Trial Limits | Key Capabilities |
| :--- | :--- | :--- | :--- | :--- |
| **Pardot (Salesforce Account Engagement)** | **Salesforce:** ~$319.95B Market Cap / ~$34.9B Revenue | **$1,250/month** (Growth+ plan, billed annually) | **No free tier; No public free trial** (access via sales-led demo and custom PoC sandbox only) | Enterprise B2B marketing automation, lead scoring/grading, and native Salesforce CRM integration for up to 10,000 prospects. |
| **Marketo Engage** | **Adobe:** ~$195.66B Market Cap / ~$21.4B Revenue | **~$895/month** (Growth tier list entry, billed annually) | **No free tier; No self-serve trial** (interactive guided tour available; custom sales demo/PoC sandbox only) | Sophisticated enterprise lead management, multi-touch attribution, ABM, and complex multi-channel campaign orchestration. |
| **HubSpot Marketing Hub** | **HubSpot:** ~$35.97B Market Cap / ~$2.63B Revenue | **$15/seat/month** (Starter tier billed annually, or $20/month billed monthly) | **Free-forever plan**: Max 2 user seats, 2,000 marketing email sends/month, 10 custom properties, HubSpot branding required, basic form follow-up automation only. | Inbound marketing, visual workflow builders, lead scoring, landing pages, and native HubSpot CRM synchronization. |
| **Zoho Marketing Automation** | **Zoho Corp:** ~$1.5B Revenue (~$10B+ Valuation) | **$19/month** (Standard plan for 1,000 contacts, billed annually) | **14-day free trial**: Full access to all product features, no credit card required upfront (no forever-free tier). | Lead nurturing journeys, dynamic email campaigns, visitor tracking, behavioral scoring, and tight Zoho CRM integration. |
| **ActiveCampaign** | **ActiveCampaign:** ~$3.0B Valuation (~$250M ARR) | **$15/month** (Starter plan for 1,000 contacts, billed annually) | **14-day free trial**: Access to Pro-tier features, 1 user seat, capped at 100 total outbound email sends, no credit card required. | Visual multi-step automations, event tracking, email marketing, SMS, and integrated lightweight CRM pipeline. |
| **Customer.io** | **Customer.io:** ~$100M+ ARR (Valuation ~$500M+) | **$100/month** (Essentials plan for 5,000 profiles, billed monthly) | **14-day free trial**: Up to 5,000 total messages across channels, max 3 recipients per test email, capped at 50 test messages/day, no credit card required. | Behavioral event-triggered messaging across email, SMS, push, and in-app for product-led growth teams. |

---

## 🟩 Open-Source Software

Self-hosted, community-driven Marketing Automation and Lead Nurturing tools. The open-source ecosystem spans **mature marketing automation platforms**, **AI-native growth platforms**, **agentic B2B CRMs**, **self-hosted email platforms with automation**, and **local-first lead generation tools**.

### Mautic
**Stack:** PHP / MySQL | **License:** GPL-3.0
Mautic is the world's largest open-source marketing automation platform, explicitly positioned for data sovereignty and privacy [citation:2]. Key capabilities include:
- **Lead management and nurturing**: Lead scoring points, triggers, and groups; stages tracking funnel position; multichannel data collection to build customer profiles [citation:2]
- **Visual campaign builder**: Drag-and-drop workflows with actions, decisions, conditions, timed delays, and Jump-to-Step routing [citation:9]
- **Dynamic segments**: Audience filters that auto-update from behavior, custom fields, tags, and point scores [citation:9]
- **Multichannel messaging**: Email, SMS, app or browser notifications out of the box, with more via plugins [citation:2]
- **Progressive profiling forms**: Dynamically show/hide fields based on known contact information, reducing abandonment [citation:2]
- **GDPR compliance**: Consent management, data erasure, audit logs, and unlimited users with role access control [citation:2]

**Critical deployment detail:** A dedicated cron worker is required for campaigns and scheduled emails to actually fire—the most common failure in self-hosted Mautic deployments [citation:11]. Deployment options include Railway templates that pre-configure the web app, cron service, and MySQL [citation:11]. Mautic is a direct alternative to HubSpot, ActiveCampaign, and Marketo, with no per-contact pricing [citation:9].
**Best for:** Organizations wanting a proven, privacy-focused marketing automation platform with full data ownership and no per-user fees, accepting the PHP/MySQL deployment and cron configuration.

### Helio
**Stack:** TypeScript / Temporal / PostgreSQL / ClickHouse | **License:** AGPL-3.0
Helio is an open-source, AI-native growth platform combining a CDP, visual journey orchestration, and multi-channel delivery [citation:5]. Key capabilities include:
- **Multi-channel**: Email, SMS (Twilio), WhatsApp (Cloud API), web push, and in-app messages [citation:5]
- **Visual journey builder**: React Flow canvas compiled to a validated DAG, with durable execution via Temporal [citation:5]
- **AI copilot**: Describe a segment, journey, or on-brand email in a sentence and get a working draft; predictive lead scoring and churn [citation:5]
- **Bring your own AI**: OpenAI, Anthropic, Groq, NVIDIA NIM, or local Ollama [citation:5]
- **MCP server**: Exposes capabilities as tools for external AI agents [citation:5]
- **CRM-lite**: Pipelines with configurable stages, task list, and meeting scheduler [citation:5]
- **Migration importers**: Detect HubSpot/Mailchimp/Klaviyo exports [citation:5]
- **Free forever**: No plans, no contact caps, no metering [citation:5]

**Best for:** Teams wanting a genuinely free, AI-native marketing automation platform with durable execution and multi-channel delivery, accepting a newer project than Mautic.

### NocoCRM
**Stack:** Node.js / NocoBase / SQLite/PostgreSQL/MySQL | **License:** Apache-2.0
NocoCRM is an open-source B2B sales CRM built on NocoBase, with **six built-in sales agents** and email/WhatsApp integration [citation:12]. Key capabilities for lead nurturing include:
- **Automatic follow-up**: New leads, new opportunities, customer replies, and daily morning checks trigger agents to read context and put the next step in your inbox—records change only when you accept [citation:12]
- **Unified timeline**: Each person connects their own email (Gmail, Microsoft 365, or any IMAP/SMTP) and the company connects WhatsApp Business [citation:12]
- **Smart capture**: Paste an email, chat, or business card, and AI turns it into leads or an opportunity for your confirmation [citation:12]
- **Company signals**: Every morning, company research searches the web for news about companies with open deals (funding, hiring, leadership changes, risks) [citation:12]
- **Approval assistance**: Approval Agent checks discounts and terms against your rules and past decisions [citation:12]
- **Full sales cycle**: Leads, companies, contacts, opportunities, tasks, approvals, and reports [citation:12]

It is **web-based** (NocoBase Admin UI) rather than a native mobile app, but its responsive interface and WhatsApp integration make it accessible on mobile browsers.
**Best for:** B2B sales teams wanting an AI-agent-driven CRM with WhatsApp integration and automated follow-ups, accepting a web-based interface rather than a native app.

### Sphericon
**Stack:** Go / PostgreSQL / React | **License:** AGPL-3.0 (open-core)
Sphericon is a self-hosted marketing automation platform with a focus on deliverability and simplicity [citation:10]. Key features include:
- **Transactional email**: Send single messages through the API [citation:10]
- **Deliverability built in**: Unsubscribes, bounces, and spam complaints honored automatically; DKIM signing; one-click unsubscribe [citation:10]
- **API and webhooks**: Workspace-scoped API with scoped tokens [citation:10]
- **Agent-ready**: MCP server lets an AI agent draft campaigns; sending stays opt-in per token [citation:10]
- **Privacy tools**: GDPR export and erasure, audit log [citation:10]
- **Multi-user workspaces**: Owners, admins, and members with two-factor sign-in [citation:10]

Deploys as a single Go binary (or Docker image) with PostgreSQL—no Redis, no object storage, no separate worker [citation:10].
**Best for:** Developers wanting a lightweight, Go-based marketing platform with strong deliverability controls and MCP integration, accepting a newer project than Mautic.

### OpenLeads
**Stack:** Python / SQLite | **License:** Open Source (PyPI)
OpenLeads is a local-first lead generation and outreach tool that runs entirely on your machine with no API keys and nothing to pay [citation:4]. Key capabilities for lead nurturing include:
- **Lead discovery**: One sentence fans out across sources—OpenStreetMap for local businesses, Y Combinator and Hacker News for startup founders, GitHub for developers, Wikidata and SEC EDGAR for companies [citation:4]
- **Evidence-based emails**: Each address is labeled with where it came from (`found`, `pattern`, or `guessed`) and a tier (`safe`, `risky`, `bad`) based on seven checks [citation:4]
- **Sequences**: Email, call, LinkedIn, and task steps with A/B variants and same-thread follow-ups; people leave when they reply, bounce, or unsubscribe [citation:4]
- **Deals pipeline**: Drag-and-drop pipeline with weighted forecast [citation:4]
- **Local workspace**: Same data in dashboard, terminal, and AI assistant [citation:4]

**Best for:** Solopreneurs and small teams wanting local-first lead generation and outreach automation without cloud dependencies or subscriptions.

### entirius-django-leads
**Stack:** Python / Django / PostgreSQL | **License:** MPL-2.0
entirius-django-leads is a Django module for leads and the B2B sales pipeline of the Entirius open-source modular ecommerce platform [citation:3]. Key capabilities include:
- **Pipeline stages**: Moves companies through configurable stages with a full activity timeline [citation:3]
- **Stage rules**: AI-assisted site analysis, recipient selection, and outreach drafts behind a consent gate [citation:3]
- **GDPR compliance**: Anonymises idle contacts on a retention schedule and serves GDPR export and erase requests [citation:3]
- **Admin API**: JWT, Pydantic schemas, OpenAPI for CMS integration [citation:3]

It runs inside the Entirius backend service (Volkanos) and drafts outreach through the communicator [citation:3].
**Best for:** Organizations building on the Entirius ecommerce platform needing B2B lead management with GDPR compliance and AI-assisted outreach.

### erxes
**Stack:** Node.js / MongoDB / React | **License:** AGPL-3.0 (Community Edition)
erxes is an open-source Experience Operating System (XOS) combining marketing, sales, operations, and support in one self-hostable platform, positioned as a HubSpot alternative [from previous context]. Key features include **Team Inbox** for real-time communication, **Leads** capture with landing pages and forms, **Engage** for email/SMS/messenger campaigns, **CRM**, **Knowledge base**, and **Sales Management** with pipeline control. It provides a **web-based CRM with mobile-responsive interfaces** rather than native apps.
**Best for:** Organizations wanting a self-hostable HubSpot alternative with sales, marketing, and support in one platform.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Lead Scoring | Visual Automation | Self-Hosted | Best For |
|----------|---------|-------|--------------|-------------------|-------------|----------|
| **HubSpot** | Proprietary | Cloud | ✅ | ✅ | ❌ | HubSpot CRM integration |
| **Marketo** | Proprietary | Cloud | ✅ | ✅ | ❌ | Enterprise B2B automation |
| **ActiveCampaign** | Proprietary | Cloud | ✅ | ✅ | ❌ | Automation depth |
| **Mautic** | GPL-3.0 | PHP/MySQL | ✅ | ✅ Campaign builder | ✅ | Proven OSS + data sovereignty |
| **Helio** | AGPL-3.0 | TypeScript/Temporal | ✅ Predictive | ✅ React Flow | ✅ | AI-native + free forever |
| **NocoCRM** | Apache-2.0 | Node.js/NocoBase | (AI agents) | (AI follow-up) | ✅ | AI-agent B2B CRM + WhatsApp |
| **Sphericon** | AGPL-3.0 | Go/Postgres | (Check) | (MCP drafts) | ✅ | Lightweight Go + deliverability |
| **OpenLeads** | Open Source | Python/SQLite | ✅ ICP fit | ✅ Sequences | ✅ (Local) | Local-first lead gen + outreach |
| **entirius-django-leads** | MPL-2.0 | Django/Postgres | (AI-assisted) | (Stage rules) | ✅ | Entirius B2B pipeline |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Marketing Automation or Lead Nurturing tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The marketing automation and lead nurturing space is **led by Mautic** for maturity and adoption (10k+ stars, active weekly development, proven as a HubSpot alternative for early-stage founders [citation:2][citation:9]). A newer generation of AI-native and agent-driven tools has emerged: **Helio** provides a free-forever growth platform with predictive lead scoring and Temporal-based durable execution [citation:5], **NocoCRM** offers six AI sales agents that handle follow-ups and company research automatically [citation:12], and **OpenLeads** provides local-first lead generation with evidence-based email labeling and outreach sequences [citation:4]. For teams wanting a lightweight Go-based platform, **Sphericon** focuses on deliverability and MCP integration [citation:10]. No single open-source project fully replicates Marketo's enterprise-scale orchestration, but these tools cover the core lead capture, scoring, and nurturing workflows for self-hosted deployments.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
