# Becoming a contributor on Askeal

Askeal is built around a community-driven contribution model. Cybersecurity organizations and experts (researchers, vendors, independent specialists, associations, etc.) can bring their knowledge into Askeal through direct content (**manual contributions**) or through their own APIs / MCP servers (**automated contributions**). This expertise is then leveraged by Askeal’s AI to provide reliable, specialized, and clearly attributed answers to users, while giving contributors visibility into the reach and usage of their expertise through dedicated analytics and metrics.

---

## 1. Why a community-driven contribution model

A reliable cybersecurity assistant requires both powerful AI and trusted knowledge. Our contribution model exists to transform the cybersecurity ecosystem’s collective expertise into structured, trusted, and traceable sources rather than relying on ad-hoc scraping.

For contributors, it is an opportunity to make their expertise visible where it matters most: directly inside the answers security professionals rely on when facing real operational challenges.

Contributors get:

- **Visibility** — their knowledge is attributed in every AI answer it powers, reaching practitioners at the exact moment they need it.
- **Direct traffic** — each attributed answer links back to the contributor's landing page, driving qualified inbound traffic from active users.
- **Analytics** — a dedicated dashboard tracks the reach, usage, and impact of contributions across the platform.
- **Revenue sharing (roadmap)** — a future version will introduce a fair revenue-sharing model allowing contributors to monetize the usage of their expertise within Askeal.

For Askeal, contributions build a managed pool of trusted and specialized sources with clear ownership and traceability — a structural advantage over generalist AI approaches.

For end users, every answer is sourced and attributed, making it possible to evaluate, verify, and trust the information they act on.

---

## 2. Vocabulary

| Term | Meaning |
| --- | --- |
| **Contributor request** | A request submitted by a user to create a contributor profile or join an existing one. |
| **Contributor profile** | An entity under which users can contribute expertise and manage contributions. |
| **Administrator** | A contributor with elevated permissions within a contributor profile. |
| **Contributor** | A regular member of a contributor profile who can add and manage contributions. |
| **Manual contribution** | Content manually added through a contributor profile, such as documents and links. |
| **Automated contribution** | An external API or MCP endpoint connected through a contributor profile and queried live by Askeal’s agents. |

---

## 3. Contributor journey

### 3.1 Creating a contributor profile
Contributor Terms are presented and linked directly in the contributor request flow before a contributor profile request can be submitted.
```text
User (logged in)
   │
   │ 1. Fills the contributor request modal
   │    (through the “Join as contributor” button
   │     or in Account settings → Contributor access → Create a new contributor profile)
   ▼
Contributor request sent to the Askeal team
   │
   │ 2. Askeal reviews and approves contributor profile requests
   ▼
On approval:
- The contributor profile is created
- The user who created it is set as its first administrator
- The administrator receives a “How to contribute” email
```

#### Key rules

- Askeal manually reviews all contributor profile creation requests before approval.
- A contributor profile can have multiple members (administrators and contributors).

---

### 3.2 Joining an existing contributor profile

A user can request access to an existing contributor profile:

- During the “Join as contributor” flow (step 4) or from:
  `Account settings → Contributor access → Request access to an existing contributor profile`

```text
User selects an existing contributor profile
   │
   │ Request submitted
   ▼
Contributor profile administrators review the request
   ▼
On approval:
- The user is added to the contributor profile as a contributor
```

#### Key rules

- Contributor profile administrators manage members of their contributor profile.

---

### 3.3 Managing a contributor profile

- **Contributor dashboard** — contribute expertise and monitor performance through analytics on reach, interest indicators, and quality scores.
- **Contributor settings** — edit the contributor profile (name, type, expertise, landing URL) and manage members (roles, statuses, deactivation).
- **Contributor profile switcher** — users who belong to multiple contributor profiles can switch context here.

---

### 3.4 Leaving or removing a contributor

- A member can leave a contributor profile from:
  `Account settings → Contributor access`
  (the last active administrator cannot leave — at least one must remain).
- An administrator can deactivate a member and change their role.
- Deleting a contributor profile is destructive: all contributions and member associations are permanently deleted.

---

## 4. Roles & permissions

| Action | Contributor | Administrator |
| --- | --- | --- |
| Access and use the contributor dashboard | ✅ | ✅ |
| View members of their contributor profiles | ✅ | ✅ |
| Accept, reject, and edit members of their contributor profiles | ❌ | ✅ |
| Edit settings of their contributor profiles | ❌ | ✅ |
| Delete their contributor profiles | ❌ | ✅ |

---
