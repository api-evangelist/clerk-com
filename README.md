# Clerk (clerk-com)

Clerk is a complete user management and authentication infrastructure platform offering embeddable UI components, flexible APIs, and admin dashboards. It provides full-stack authentication including multi-factor authentication, social sign-on, passkeys, organizations for B2B SaaS, billing, session management, and machine-to-machine authentication, with SDKs spanning Next.js, React, Expo, iOS, Android, Go, Python, Ruby, Java, PHP, and C#.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/clerk-com/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/clerk-com/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Authentication
- Authorization
- B2B SaaS
- CIAM
- Identity Management
- MFA
- OAuth
- OpenID Connect
- Organizations
- Passkeys
- SAML
- Security
- Sessions
- SSO
- User Management

## Timestamps

- **Created:** 2026-05-22
- **Modified:** 2026-05-22

## APIs

### Clerk Backend API

The Clerk Backend API is a REST API meant to be accessed by backend servers. It exposes resources for managing users, sessions, organizations, invitations, JWT templates, OAuth applications, SAML connections, M2M tokens, API keys, and billing — wrapped by every official Clerk backend SDK.

- **Human URL:** [https://clerk.com/docs/reference/backend-api](https://clerk.com/docs/reference/backend-api)
- **Base URL:** `https://api.clerk.com/v1`

#### Tags

- Authentication
- Backend
- Identity Management
- REST
- User Management

#### Properties

- [Documentation](https://clerk.com/docs/reference/backend-api)
- [API Reference](https://clerk.com/docs/reference/backend-api)
- [OpenAPI](openapi/clerk-backend-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clerk-backend-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk-backend-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Getting Started](https://clerk.com/docs/quickstarts/overview)
- [Authentication](https://clerk.com/docs/backend-requests/making/jwt-templates)
- [Spectral Ruleset](rules/clerk-rules.yml)

### Clerk Frontend API

The Clerk Frontend API powers Clerk's prebuilt UI components and JavaScript SDKs. It handles sign-in, sign-up, session, organization, passkey, multi-factor, billing, and waitlist flows directly from browser, mobile, and chrome-extension contexts.

- **Human URL:** [https://clerk.com/docs](https://clerk.com/docs)
- **Base URL:** `https://{domain}.clerk.accounts.dev`

#### Tags

- Authentication
- Frontend
- JavaScript
- Sessions
- Sign-In
- Sign-Up

#### Properties

- [Documentation](https://clerk.com/docs)
- [OpenAPI](openapi/clerk-frontend-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clerk-frontend-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk-frontend-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Platform API

The Clerk Platform API (beta) is a partner / reseller surface for programmatically creating and managing Clerk applications, domains, application transfers, users, JWT templates, redirect URLs, and platform configuration on behalf of end customers.

- **Human URL:** [https://clerk.com/docs](https://clerk.com/docs)
- **Base URL:** `https://api.clerk.com/v1`

#### Tags

- Applications
- Beta
- Multi-Tenant
- Partner
- Platform

#### Properties

- [Documentation](https://clerk.com/docs)
- [OpenAPI](openapi/clerk-platform-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clerk-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Webhooks

Clerk Webhooks deliver real-time events for users, sessions, organizations, invitations, email, SMS, and SAML changes via Svix, allowing applications to react asynchronously to identity lifecycle events.

- **Human URL:** [https://clerk.com/docs/webhooks/overview](https://clerk.com/docs/webhooks/overview)
- **Base URL:** `https://api.clerk.dev/v1`

#### Tags

- Events
- Svix
- Webhooks

#### Properties

- [Documentation](https://clerk.com/docs/webhooks/overview)
- [OpenAPI](openapi/clerk-webhooks-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/clerk-webhooks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Homepage](https://clerk.com)
- [Documentation](https://clerk.com/docs)
- [Sign Up](https://dashboard.clerk.com/sign-up)
- [Sign In](https://dashboard.clerk.com/sign-in)
- [Pricing](https://clerk.com/pricing)
- [Terms of Service](https://clerk.com/terms)
- [Privacy Policy](https://clerk.com/privacy)
- [Security](https://clerk.com/security)
- [Blog](https://clerk.com/blog)
- [Changelog](https://clerk.com/changelog)
- [Changelog R S S](https://clerk.com/changelog/atom.xml)
- [Status Page](https://status.clerk.com)
- [Support](https://clerk.com/support)
- [Git Hub](https://github.com/clerk)
- [Open A P I Repository](https://github.com/clerk/openapi-specs)
- [X (Twitter)](https://x.com/ClerkDev)
- [SDK](https://github.com/clerk/javascript)
- [SDK](https://github.com/clerk/clerk-sdk-go)
- [SDK](https://github.com/clerk/clerk-sdk-python)
- [SDK](https://github.com/clerk/clerk-sdk-ruby)
- [SDK](https://github.com/clerk/clerk-sdk-java)
- [SDK](https://github.com/clerk/clerk-sdk-php)
- [SDK](https://github.com/clerk/clerk-sdk-csharp)
- [SDK](https://github.com/clerk/clerk-ios)
- [SDK](https://github.com/clerk/clerk-android)
- [SDK](https://github.com/clerk/clerk-sdk-flutter)
- [C L I](https://github.com/clerk/cli)
- [C L I](https://github.com/clerk/protect-cli)
- [Integration](https://clerk.com/docs/integrations/databases/supabase)
- [Integration](https://clerk.com/docs/integrations/databases/convex)
- [Integration](https://vercel.com/integrations/clerk)
- [Tool](https://github.com/clerk/agent-toolkit-example)
- [Tool](https://github.com/clerk/agentpass)
- [Tool](https://github.com/clerk/mcp-tools)
- [Tool](https://github.com/clerk/migration-tool)
- [Plans](plans/clerk-com-plans-pricing.yml)
- [Rate Limits](rate-limits/clerk-com-rate-limits.yml)
- [Fin Ops](finops/clerk-com-finops.yml)
- [Vocabulary](vocabulary/clerk-com-vocabulary.yml)
- [JSON-LD](json-ld/clerk-com-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/clerk-user-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-user-structure.json)
- [JSON Schema](json-schema/clerk-session-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-session-structure.json)
- [JSON Schema](json-schema/clerk-organization-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-organization-structure.json)
- [JSON Schema](json-schema/clerk-organizationmembership-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-organizationmembership-structure.json)
- [JSON Schema](json-schema/clerk-organizationinvitation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-organizationinvitation-structure.json)
- [JSON Schema](json-schema/clerk-invitation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-invitation-structure.json)
- [JSON Schema](json-schema/clerk-emailaddress-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-emailaddress-structure.json)
- [JSON Schema](json-schema/clerk-phonenumber-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-phonenumber-structure.json)
- [JSON Schema](json-schema/clerk-client-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-client-structure.json)
- [JSON Schema](json-schema/clerk-oauthapplication-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-oauthapplication-structure.json)
- [JSON Schema](json-schema/clerk-samlconnection-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-samlconnection-structure.json)
- [JSON Schema](json-schema/clerk-jwttemplate-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-jwttemplate-structure.json)
- [JSON Schema](json-schema/clerk-signintoken-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-signintoken-structure.json)
- [JSON Schema](json-schema/clerk-actortoken-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/clerk-actortoken-structure.json)
- [L L Ms Txt](https://clerk.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
