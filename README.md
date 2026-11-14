# Vittoria

**Conversational scheduling for service businesses: book, reschedule and cancel appointments through chat, with human handoff and access control built in.**

> **Showcase only.** This repository presents the Vittoria product to prospective partners and customers. It contains **no source code** and **grants no license** of any kind. See [Notice](#notice).

Português: [README.pt-BR.md](README.pt-BR.md)

---

## What Vittoria is

Vittoria is a multi-tenant assistant that lets customers of a service business manage their appointments in a chat conversation. A business keeps its own agenda, rules and users; the assistant handles the repetitive scheduling dialogue and hands the conversation to a person when needed.

## Development stage

Vittoria is **under active development**. The capabilities below have been exercised in a **development environment with fictitious data and automated tests**. They are **not** presented as certified, audited or production-proven, and this page makes no claim about production use.

| Capability | Stage |
|---|---|
| Appointment booking, rescheduling and cancellation by conversation | Working in development; tested with synthetic data |
| Human handoff | Working in development; tested with synthetic data |
| Multi-tenant operation (separate data per business; isolation tested) | Working in development; tested with synthetic data |
| Access control for administrators and operators | Working in development; tested with synthetic data |
| Encrypted, verified backups of business databases | Working in development; tested with synthetic data (automatic backup scheduling still pending) |
| Message-handling logs limited to fixed categories (no message text, phone numbers or identifiers) | Working in development; covered by automated tests |
| Signed, size- and rate-limited inbound webhooks | Working in development |
| Time zones per business (including daylight-saving edge cases) | Tested with synthetic data; one zone used in early trials |
| Portuguese (Brazil) as reference language | Working in development |
| English and Spanish | **Experimental** — pending native-speaker review |
| WhatsApp delivery through the official Meta Business Cloud API | **Under validation** — not announced as operational |
| Dashboards, billing, additional channels | **Planned** — not available |

## Conceptual architecture

```
 Customer chat channel
          |
          v
   Secure message intake  (authentication, validation, limits)
          |
          v
   Dialogue engine  <---->  Language layer (catalogs, formatting)
          |
          v
   Scheduling service  <---->  Per-business data store (encrypted backups)
          |
          v
   Human handoff / administration (access-controlled)
```

Each business ("tenant") has isolated data and settings. Implementation details are intentionally not published.

## Commercial opportunities

We are interested in conversations with companies about:

- **Demonstrations** with fictitious data.
- **Partnerships** (implementation, integration, referral).
- **Licensing, managed service, deployment and support** models.

All of the above are **subject to formal agreements**. Nothing in this repository is an offer, a price list or a contract.

## Contact

Commercial contact: to be announced.

## Notice

- This repository is a **showcase**. It does not provide source code, binaries, installers or documentation sufficient to run the product.
- **No license** is granted — no open-source license, no right to use, copy, modify or distribute any product software, and no trademark rights. All rights are reserved by their respective holders.
- Descriptions reflect the development state at publication time and may change without notice. Statements about stages above are not warranties or commitments.
- Names and marks mentioned (for example WhatsApp and Meta) belong to their owners; no affiliation, endorsement or official partnership is claimed.
