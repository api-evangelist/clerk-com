# Clerk — API Evangelist Profile

[Clerk](https://clerk.com) is a complete user management and authentication infrastructure platform built around embeddable UI components, flexible REST APIs, and admin dashboards. Clerk offers full-stack authentication and identity management — multi-factor authentication, social SSO, passkeys, organizations for B2B SaaS, billing, session management, and machine-to-machine authentication — wrapped by SDKs spanning Next.js, React, Expo, iOS, Android, Go, Python, Ruby, Java, PHP, and C#.

This repository profiles Clerk's developer surface using the [APIs.json](https://apisjson.org) format. It catalogs every public API surface, downloads canonical OpenAPI specs, generates Naftiko capabilities, JSON Schemas, JSON-LD, vocabulary, Spectral rules, and aligns Clerk's commercial offering to the API Commons Plans, Rate Limits, and FOCUS FinOps specifications.

## APIs Documented

| API | Description | Spec |
|---|---|---|
| **Clerk Backend API** | REST API for backend servers (155 ops): users, sessions, organizations, invitations, JWT templates, OAuth applications, SAML connections, M2M tokens, API keys, billing. | [`openapi/clerk-backend-api-openapi.yml`](./openapi/clerk-backend-api-openapi.yml) |
| **Clerk Frontend API** | Browser/mobile/chrome-extension surface (150 ops) powering Clerk's prebuilt sign-in, sign-up, session, organization, passkey, MFA, billing, and waitlist flows. | [`openapi/clerk-frontend-api-openapi.yml`](./openapi/clerk-frontend-api-openapi.yml) |
| **Clerk Platform API (Beta)** | Partner/reseller surface (26 ops) for creating and managing Clerk applications, domains, transfers, users, JWT templates, and platform config. | [`openapi/clerk-platform-api-openapi.yml`](./openapi/clerk-platform-api-openapi.yml) |
| **Clerk Webhooks** | Svix-delivered event stream for user, session, organization, invitation, email, SMS, and SAML lifecycle events. | [`openapi/clerk-webhooks-openapi.yml`](./openapi/clerk-webhooks-openapi.yml) |

All four specs are pulled from Clerk's canonical [`clerk/openapi-specs`](https://github.com/clerk/openapi-specs) GitHub repository at version `2025-11-10` (BAPI + FAPI), `beta` (Platform), and `2025-04-15` (Webhooks).

## Repository Layout

```
clerk-com/
├── apis.yml                  Top-level APIs.json index
├── README.md                 This file
├── openapi/                  4 OpenAPI 3 specs (BAPI, FAPI, Platform, Webhooks)
├── rules/                    Spectral ruleset enforcing Clerk's conventions
├── capabilities/             87 Naftiko capability YAMLs (84 per-tag + 3 workflow compositions)
├── json-schema/              14 entity JSON Schemas (Draft 2020-12)
├── json-structure/           14 structural overlays per entity
├── json-ld/                  JSON-LD context mapping Clerk vocab to schema.org
├── examples/                 26 example payloads (canonical entities + response samples)
├── vocabulary/               Operational vocabulary, dimensions, and ID-prefix taxonomy
├── plans/                    Pricing/plans aligned to API Commons Plans 0.1
├── rate-limits/              Rate-limit policies aligned to API Commons Rate Limits 0.1
└── finops/                   FOCUS-aligned FinOps view of Clerk billing
```

## Pricing at a Glance

Source: [clerk.com/pricing](https://clerk.com/pricing) snapshot 2026-05-22.

| Plan | Price (annual / monthly) | Included MRUs | Highlights |
|---|---|---|---|
| Hobby | Free | 50,000 | Unlimited apps, 3 dashboard seats, Clerk branding |
| Pro | $20 / $25 per month | 50,000 | No branding, MFA, passkeys, custom email templates |
| Business | $250 / $300 per month | inherits Pro | 10 seats, SOC2 report, priority support, 30-day log retention |
| Enterprise | Custom | Custom | 99.99% uptime SLA, HIPAA, dedicated support |

Add-ons:
- **B2B Authentication Enhanced** — $85 / $100 per month, unlocks unlimited org members and custom role sets.
- **Administration Enhanced** — $85 / $100 per month, unlimited user impersonations.
- **Billing** — 0.7% of billing volume + Stripe fees.
- **API Keys / M2M** — Free up to 1,000 monthly creations, then $0.001 per creation.

Full breakdown in [`plans/clerk-com-plans-pricing.yml`](./plans/clerk-com-plans-pricing.yml).

## Capabilities

87 [Naftiko](https://github.com/naftiko) capability files are generated under `capabilities/`:

- **38 Backend-API capabilities** — one per OpenAPI tag (Users, Sessions, Organizations, Organization Memberships, Organization Invitations, Organization Roles, Organization Permissions, Organization Domains, Role Sets, Invitations, Email Addresses, Phone Numbers, Clients, JWT Templates, JWKS, OAuth Applications, OAuth Access Tokens, SAML Connections, Enterprise Connections, M2M Tokens, API Keys, Machines, Sign-in Tokens, Actor Tokens, Sign Ups, Testing Tokens, Agent Tasks, Allow-list / Block-list, Redirect URLs, Domains, Email & SMS Templates, Instance Settings, Webhooks, Beta Features, Waitlist Entries, Proxy Checks, Accountless Applications, Billing, Miscellaneous).
- **39 Frontend-API capabilities** — one per Frontend API tag (Client, Sessions, Sign Ins, Sign Ups, User, Email Addresses, Phone Numbers, Passkeys, External Accounts, TOTP, Backup Codes, Active Sessions, Web3 Wallets, OAuth2 Identity Provider, OAuth2 Callbacks, SAML, Plans, Subscriptions, Subscription Items, Checkouts, Payment Methods, Payment Attempts, Statements, Organization, Organization Creation Defaults, Organizations Memberships, Invitations, Members, Membership Requests, Domains, Environment, Waitlist, API Keys, Enterprise Connections, Health, Well Known, DevBrowser, DevTools, Miscellaneous).
- **7 Platform-API capabilities** — Applications, Domains, Application Transfers, Users, JWT Templates, Redirect URLs, Config.
- **3 workflow compositions** — [`clerk-user-lifecycle.yaml`](./capabilities/clerk-user-lifecycle.yaml), [`clerk-b2b-saas.yaml`](./capabilities/clerk-b2b-saas.yaml), [`clerk-machine-to-machine.yaml`](./capabilities/clerk-machine-to-machine.yaml).

## SDK & Tooling Surface

Clerk's [GitHub org](https://github.com/clerk) (`149 public repos`) exposes a deep first-party SDK matrix:

**Backend SDKs** — Go, Python, Ruby, Java, PHP, C# / .NET.
**Mobile / Edge SDKs** — iOS (Swift), Android (Kotlin), Flutter (Dart), Chrome Extension.
**Frontend SDKs (monorepo)** — Next.js, React, Astro, Remix, Vue, Nuxt, Expo, React Router, TanStack React Start.
**CLIs** — [`clerk/cli`](https://github.com/clerk/cli) (agentic CLI), [`clerk/protect-cli`](https://github.com/clerk/protect-cli) (early access).
**Agent / MCP tooling** — [`clerk/agentpass`](https://github.com/clerk/agentpass), [`clerk/mcp-tools`](https://github.com/clerk/mcp-tools), [`clerk/mcp-nextjs-example`](https://github.com/clerk/mcp-nextjs-example), [`clerk/skills`](https://github.com/clerk/skills).
**Migration / Eval** — [`clerk/migration-tool`](https://github.com/clerk/migration-tool), [`clerk/clerk-evals`](https://github.com/clerk/clerk-evals).

## Operational Signals

- **Versioning** — Clerk uses date-based API versions (`2024-10-01`, `2025-11-10`). Five published versions of the Backend and Frontend APIs are tracked in `clerk/openapi-specs`.
- **Status** — [status.clerk.com](https://status.clerk.com) tracks 11 production, 1 development, and 4 administration components, reporting 99.95% uptime for Feb–May 2026.
- **Changelog** — Atom feed at [`clerk.com/changelog/atom.xml`](https://clerk.com/changelog/atom.xml). Recent themes: SCIM directory sync GA (May 2026), Application Logs launch, Clerk CLI, M2M / API Keys GA, native iOS/Android theming.
- **Compliance** — SOC2 Type II (Business+), HIPAA available (Enterprise), GDPR/CCPA.

## API Versions Tracked

| Surface | Versions in `clerk/openapi-specs` |
|---|---|
| BAPI (Backend) | `2021-02-05`, `2024-10-01`, `2025-03-12`, `2025-04-10`, `2025-11-10` |
| FAPI (Frontend) | `2021-02-05`, `2024-10-01`, `2025-03-12`, `2025-04-10`, `2025-11-10` |
| Platform | `beta` |
| Webhooks | `2025-04-15` |

This repo tracks the latest in each lane.

## License & Maintainer

This profile is maintained by [Kin Lane](https://x.com/apievangelist) (API Evangelist / Naftiko) under the [API Evangelist Network](https://github.com/api-evangelist). Profile data is licensed CC-BY 4.0; Clerk's canonical OpenAPI specs remain under the MIT license stated in [`clerk/openapi-specs`](https://github.com/clerk/openapi-specs/blob/main/LICENSE).
