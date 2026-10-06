---
name: app-legal-risk-check
description: Check six legal risk areas when building web apps, preparing launches, or changing signup, fonts, session replay, marketing email, subscriptions, or user uploads. Implement authorized technical fixes and report applicability and evidence for all six areas.
---

# App Legal Risk Check

Always account for all six areas below when this skill is invoked. For new apps, check before completion. For relevant changes, reuse valid evidence and rerun affected checks. Do not restart a full audit for unrelated minor edits. This is a technical risk review, not comprehensive legal advice or a compliance certification. Respond in the user's language.

## Workflow

1. Establish the operator, markets served, intended ages, data flows, and relevant features from the project and user context. Language, operator location, or public accessibility alone does not establish jurisdiction. Mark unknowns; ask only for information needed for a dependent decision and continue independent work.
2. Inspect code, dependencies, configuration, accessible provider settings, and runtime behavior. A dependency does not prove active recording; an empty code search does not prove absence. Include tag managers, embeds, OAuth, and hosted checkout.
3. Read [legal sources](references/legal-sources.md) for applicable legal claims and verify current primary sources, effective dates, and transition rules. If verification is unavailable, say so and continue technical work. Do not turn social-media penalty figures into automatic liability estimates.
4. Implement appropriate reversible fixes within an implementation request. An audit-only request remains an audit. Never invent an address, price, age policy, registration, or consent. Missing business facts prevent clearing the affected flow; placeholders are not completed fixes.
5. Report all six areas as **checked**, **fixed and verified**, **action needed**, **unknown/unverified**, or **not applicable**. Explain non-applicability. Include applicability, evidence (file/line, setting, or runtime test), changes, and remaining work. Separate technical findings from legal uncertainty; never label the app universally compliant.

Invoking this skill alone does not authorize publishing, marketing sends, payments, or government filings. Existing authorization remains valid. Prepare concrete external steps before requesting any genuinely missing authorization. Do not seek repeated approval for routine authorized code fixes.

## 1. Signup, children, and COPPA

- Distinguish US applicability, child-directed services, mixed-audience services, and actual knowledge of collection from children under 13. A missing age field alone is not a COPPA violation; adding a checkbox alone does not establish compliance.
- Where appropriate and required, use neutral, data-minimizing age screening before relevant collection. Avoid unnecessary ID documents or full birth dates. Do not exclude children from a primarily child-directed service merely to evade COPPA; treat required parental consent as a real product requirement.
- Where applicable, check parental notices and rights, minimization, deletion, retention, and third parties. Assess other applicable age/consent rules separately; do not apply the US threshold globally.
- **Verify:** direct API calls and OAuth cannot bypass implemented protections. Inspect storage and SDK/analytics initialization before age or parental approval. Use synthetic data for boundary cases.

## 2. Remote fonts and privacy

- Check HTML, CSS, imports, themes, widgets, preloads, preconnects, and browser requests for `fonts.googleapis.com`, `fonts.gstatic.com`, and other font providers. Distinguish build-time downloads from browser disclosures.
- Prefer licensed self-hosting or existing system fonts for remote browser loads. Preserve design, required weights, language coverage, and license notices; remove unnecessary external connections. Do not flag locally served Google Fonts solely because of their name.
- **Verify:** use a fresh browser session without cache across relevant pages and embeds. Confirm no residual remote font requests, missing files, or typography regressions. Self-hosting resolves this data flow, not all privacy obligations.

## 3. Session replay, inputs, and CIPA

- Inspect SDKs, tag managers, client/server activation, sampling, and provider defaults. Examples include Hotjar, FullStory, Clarity, LogRocket, rrweb, PostHog Replay, and Sentry Replay. DOM text, URLs, network payloads, and hidden fields may expose sensitive information too.
- Disable unnecessary replay. If replay is wanted, implement explicit prior consent, effective withdrawal, masking before capture/transmission, and exclusions for sensitive pages/fields. A banner without an SDK gate is insufficient. Masking does not replace consent; consent alone does not establish legal compliance.
- **Verify:** fresh visit, rejection, acceptance, withdrawal, and navigation. No replay collection/transmission before consent or after withdrawal. Inspect recorded payloads using synthetic secrets to confirm inputs, tokens, payment details, and health data are excluded. Assess CIPA based on the facts, not an automatic dollar amount per session.

## 4. Marketing email and CAN-SPAM

- Inspect all commercial templates and sending paths, including launch announcements. Classify transactional messages by their actual primary purpose, not their name.
- Check accurate sender/subject information, required advertising identification, a genuine valid postal address, and a clear working opt-out. Prefer a visible unsubscribe link in HTML and plain text. No login, fee, or unnecessary information; enforce suppression across marketing senders.
- CAN-SPAM does not replace consent requirements under other applicable rules. Possessing an email address is not blanket marketing permission.
- **Verify:** rendered templates, test-system opt-out, repeated opt-out, and suppression for future/queued sends. The FTC guidance states that the mechanism must work for at least 30 days after sending and requests must be honored within 10 business days; prefer immediate technical suppression. Recheck current requirements. Do not send real campaigns to test.

## 5. Subscriptions and automatic renewal

- Clearly show actual price, currency, billing interval, automatic renewal, trial conversion price, and cancellation conditions near the binding consent action. A terms link alone is not a substitute. Match payment-provider configuration; include mobile and hosted checkout.
- Check applicable express/separate consent, evidence, retainable confirmation, cancellation, and renewal/change notices. Consider California transition rules, contract dates, and other relevant markets. Do not infer an automatic SaaS refund from any missing button disclosure.
- **Verify:** sandbox checkout, consent without preselection, correct confirmation, and a reachable cancellation flow that actually stops further renewals. Do not make real charges or refunds for testing. Mark inaccessible provider settings as unverified.

## 6. User uploads and DMCA

- Inspect user content, public/private uploads, hosting/linking features, and US relevance. Separate rights to the operator's own content from safe harbor for third-party content. Explain non-applicability rather than adding an unnecessary registration flow.
- For relevant protection under 17 USC §512(c), check registration and public agent contact information. Registration alone is insufficient: assess notice-and-takedown, counter-notice handling, a reasonably implemented repeat-infringer policy, and other statutory conditions.
- If registration is missing, guide the user through official steps: search the directory; prepare the legal operator, alternate names/domains, and agent contacts; identify information that becomes public; show the official filing route and current fee; after authorized filing, verify the directory entry against the website. Document renewal timing; create reminders only if requested. Use the linked source reference for details.
- **Verify:** available directory records, public contact page, and the internal reporting/handling process with test data. Do not send real takedown notices. A footer link does not establish registration. A missing agent does not automatically establish liability or a fixed penalty per upload.

## Final report

Provide a concise table with exactly six areas, statuses, and evidence. Follow with only concrete unresolved decisions, external steps, or unperformed tests. Update existing project documentation when durable and useful. Completion means all six areas were assessed transparently, not that every app must implement all six features.
