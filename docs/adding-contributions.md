# Adding contributions & monitoring performance

Once a contributor profile is approved, its members can share their expertise to Askeal through two contribution methods.

---

## What content can be contributed

Contributors can only submit content they are authorized to share and use within Askeal.

This includes:
- content they created themselves;
- company-owned content they are authorized to contribute;
- public content they have permission or rights to use;
- APIs or MCP servers they operate or are authorized to expose through Askeal.

Examples of accepted contributions include:
- cybersecurity research and reports;
- anonymized pentest reports;
- malware analysis;
- vulnerability PoCs;
- threat intelligence;
- playbooks and detection rules;
- technical knowledge bases;
- APIs exposing cybersecurity intelligence or capabilities.

Contributors remain owners of their content at all times.

Askeal does not:
- take ownership of contributed content;
- sell contributed content independently from the platform;
- use contributed content to train LLMs.

Contributors are responsible for ensuring that:
- the content does not infringe third-party rights;
- they have the necessary authorizations to share it;
- confidential or sensitive information has been properly removed or anonymized when required.

---

## 1. Manual contributions

A manual contribution is a piece of cybersecurity expertise manually shared through a document or a link. This can include cybersecurity reports, anonymized pentest reports, malware discoveries, vulnerability PoCs, research articles, threat intelligence content, playbooks, or other specialized resources.

### How manual contributions are added

From:
`Contributor dashboard → Manual contributions → Add content`

1. The contributor fills in the contribution information:
   - Name
   - Category
   - Description

   This information must be properly completed to facilitate contribution review and approval.

2. The contributor chooses one of two input modes:
   - **Document upload** — one or more files in `PDF`, `DOCX`, `TXT`, or `MD` format, up to `20 MB` per file.
   - **Article URL** — a link to a public article or page.

3. The contribution goes through automated quality and security checks before being approved or rejected.

Contributors can edit contribution metadata (name, category, description) or delete contributions at any time.

---

## 2. Automated contributions

An automated contribution is an external HTTP API (or MCP server) that Askeal calls when its users look for this type of expertise.

### How automated contributions are added

From:
`Contributor dashboard → Automated contributions → Connect an API`

The setup process is divided into three steps:

1. **Getting started**

2. **API configuration** — technical setup including:
   - Name and description — *Mandatory*
   - HTTP method (`GET`, `POST`, `PUT`, `PATCH`, `DELETE`) — *Mandatory*
   - URL, headers, query parameters, and request body — *Optional*
   - Authentication (`none`, `Bearer token`, or `API key`) — *Optional*

3. **Usage tiers** — contribution limits configured by the contributor:
   - **Freemium tier** — usage cap or unlimited access
   - **Premium tier** — will be enabled once Askeal launches paid plans and the revenue-sharing model
   - **Advanced** — optional global hard cap

Before saving, Askeal performs a **test call** to validate the configuration and ensure the endpoint responds correctly.

Automated contributions can later be edited, disabled, or deleted by contributor profile administrators.

### Automated contribution specific metrics

| Metric | What it measures |
| --- | --- |
| **Status** | API health tracking: `Healthy` (<10% errors), `Warning` (10–30%), or `Error` (≥30%). |
| **Responses provided** | Total number of calls made by Askeal to the API. |
| **Responses used** | Calls whose response was actually used by the AI in an answer. |
| **Average response time** | Average API latency observed by Askeal. |
| **Error rate** | Share of failed calls (HTTP error, timeout, malformed response, etc.). |

---

## 3. Contributor dashboard metrics

The contributor dashboard aggregates metrics across all contributions for the selected contributor profile and time range (`7 days`, `30 days`, `all time`, or custom range).

Available metrics include:

- **Reach** — total number of times the contributor profile’s expertise was surfaced or used across the platform.
- **Marks of interest** — number of interactions with the contributor profile’s landing page or expertise.
- **Quality score** — overall satisfaction score based on user feedback on contributions.
- **Positive and negative feedback** — distribution of end-user feedback on contributions.
- **API health** — overall health status of automated contributions.
- **API performance metrics** — per-API monitoring including responses provided, responses used, average response time, and error rate.
- **Earnings** — future revenue tracking linked to the upcoming revenue-sharing model for premium tiers.

---

## 4. Visibility & access control

- All metrics are scoped to the current contributor profile — contributors only access data related to profiles they belong to.
- Users who belong to multiple contributor profiles can switch context through the contributor profile switcher.
- End users never access contributor dashboards. They only see contributor profiles as attributed sources inside AI answers.

---

## 5. Related documentation

The contributor system is documented across several complementary pages:

- [contributing-to-askeal.md](./contributing-to-askeal.md) — contributor profiles, roles, permissions, onboarding flows, and contributor management.
- [adding-contributions.md](./adding-contributions.md) — how contributors add manual or automated contributions and monitor their performance.
- [manual-rag.md](./contribution-processing.md) — how manually added content is processed and used by Askeal’s AI.
