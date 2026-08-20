# PromptShields documentation

Source for [docs.promptshields.com](https://docs.promptshields.com), built with [Mintlify](https://mintlify.com).

Audience: IT admins, endpoint engineers, and security leads deploying and running PromptShields.

## Structure

| Path | Contents |
| --- | --- |
| `docs.json` | Site config and navigation |
| `introduction.mdx` | Entry point — what the product is and a rollout sequence |
| `how-it-works.mdx` | The detection and telemetry pipeline end to end |
| `data-handling.mdx` | What is collected, what never leaves the device, storage per platform |
| `deploy/` | Browser extension, macOS agent, Windows agent, MDM rollout |
| `admin/` | Identity and access, policies, monitoring and reporting, integrations |
| `troubleshooting.mdx` | Cross-client failure modes |

## Local preview

```bash
npx mint@latest dev
```

Check links before publishing:

```bash
npx mint@latest broken-links
```

## Publishing

Commits to `main` deploy automatically to docs.promptshields.com.

## House rules

- **Never document prompt content flowing anywhere.** It does not, and the docs must not imply otherwise.
- Mark unreleased integrations as *Planned* or *In development*. Do not describe roadmap work as shipped.
- Keep internal material — roadmap phases, customer names, pricing strategy, PR numbers — out of this repo.
