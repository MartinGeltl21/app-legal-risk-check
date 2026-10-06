# App Legal Risk Check

A reusable agent skill for checking six legal risk areas in web apps and verifying practical technical fixes.

[Deutsch](README.de.md) · [Skill instructions](SKILL.md) · [Primary sources](references/legal-sources.md) · [MIT license](LICENSE)

Use it when building an app, reviewing a launch, or changing a relevant feature. Every invocation accounts for all six areas, including a reason when something does not apply.

| Area | What the agent checks |
| --- | --- |
| Signup / COPPA | Audience, relevant age and parental-consent flows, early data collection |
| Remote fonts / privacy | Browser disclosures, licensed self-hosting, residual requests |
| Session replay / CIPA | Activation, consent, withdrawal, sensitive-data masking |
| Marketing / CAN-SPAM | Sender information, postal address, functional unsubscribe and suppression |
| Subscriptions | Renewal disclosures, consent, confirmation, cancellation |
| User uploads / DMCA | Relevant agent registration, public contacts, notice-handling processes |

This is an instruction-only skill: no executable scanner, dependencies, telemetry, or required API keys. The host agent needs project access and appropriate tools to inspect code, test behavior, and verify current sources. It reports inaccessible settings or unperformed tests rather than claiming success.

## Install in Codex

Ask the built-in installer:

```text
Use $skill-installer to install the skill from
https://github.com/MartinGeltl21/app-legal-risk-check
The SKILL.md is at the repository root.
```

Or clone it into a personal skill directory. Requires Git; the target folder must not already exist.

**macOS / Linux**

```sh
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/MartinGeltl21/app-legal-risk-check.git "$HOME/.agents/skills/app-legal-risk-check"
```

**Windows PowerShell**

```powershell
$skillRoot = Join-Path $env:USERPROFILE '.agents/skills'
New-Item -ItemType Directory -Force -Path $skillRoot | Out-Null
git clone https://github.com/MartinGeltl21/app-legal-risk-check.git (Join-Path $skillRoot 'app-legal-risk-check')
```

For project-only use, place the folder at `.agents/skills/app-legal-risk-check` inside your project. Avoid duplicate installations under the same skill name. If discovery does not refresh, restart Codex. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills).

## Use

**Audit only**

```text
Use $app-legal-risk-check to audit this app. Do not edit files.
Report all six areas with applicability, evidence, and remaining work.
```

**Audit and fix**

```text
Use $app-legal-risk-check before launch. Implement applicable technical
fixes, test the affected flows, and report any external steps I must complete.
```

The skill responds in your language. Automatic selection is enabled for matching tasks, but host selection is not a guaranteed execution hook. Invoke it explicitly when you need the check to run. It respects audit-only requests and existing authorization boundaries.

## What you get

A six-row report with **checked**, **fixed and verified**, **action needed**, **unknown/unverified**, or **not applicable**, backed by code locations, settings, or runtime evidence. Relevant checks include fresh-session network requests, consent rejection/withdrawal, unsubscribe suppression, and sandbox checkout/cancellation.

## Scope and limitations

This is a technical review aid, not legal advice or a compliance certification. Applicability depends on the product, users, markets, and facts. It does not blindly add age gates or calculate automatic fines from a viral post. The source reference is dated and requires current verification; it is not automatically maintained. Other legal obligations may apply outside these six areas.

External source pages are references and remain subject to their respective terms. This project is independent and is not endorsed by OpenAI or any regulator.

## Contributing

Issues and pull requests are welcome. For legal corrections, include a primary source, jurisdiction, and effective date. For workflow changes, explain a concrete failure and how the change helps. Preserve all six areas, audit-only behavior, authorization boundaries, and explicit reporting of uncertainty. Keep the skill instruction-only unless a helper has a demonstrated benefit.

Do not post credentials, customer records, or private legal documents in issues. Keep this README and [the German overview](README.de.md) consistent.

## License

[MIT](LICENSE). You may use, modify, and redistribute the skill, including commercially, subject to the license terms.
