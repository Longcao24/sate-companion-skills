# SATE Companion Skills

Agent skills for working on the **SATE Companion** system — a speech-capture and analysis
platform for speech-language pathologists: an ESP32-S3 **recorder**, an nRF52840 **pendant**,
a React Native **mobile app**, a React/Vite **web app**, and a Supabase + Cloudflare **backend**.

By the end of a session, your coding agent should be able to:

- [ ] Build, flash, and cut releases for the recorder and pendant firmware
- [ ] Run and deploy the mobile app, web app, and docs site
- [ ] Deploy the backend edge functions and the async AI pipeline correctly
- [ ] Avoid the failures that **permanently brick a Plaud device**, break the shared BLE radio,
      hang the AI pipeline, or lose a patient's recording

## Installation

### Skills CLI (recommended)

The [Skills CLI](https://github.com/vercel-labs/skills) adds these skills to your coding agent
automatically:

```bash
npx skills add Longcao24/sate-companion-skills
```

Update later with:

```bash
npx skills update
```

### Manual installation

Copy the skill folder into your agent's skills directory:

```bash
# Claude Code (project-local)
cp -r skills/sate-companion-dev-skill .claude/skills/

# Claude Code (global, all projects)
cp -r skills/sate-companion-dev-skill ~/.claude/skills/
```

Cursor uses `~/.cursor/skills/`; other agents use `~/.config/agents/skills/`. Claude Code
picks up the skill on the next session.

## What's inside

| Skill | Covers |
|---|---|
| **sate-companion-dev-skill** | The whole product. A mandatory 5-row pre-flight review, a common-tasks index, the real build/flash/run/deploy commands, and reference playbooks for the safety invariants, build/flash/release, and the async backend + hardware-in-the-loop testing. |

## Source of truth

Deep, line-precise detail lives in the main product repo
([Longcao24/sate-companion](https://github.com/Longcao24/sate-companion)) — its `CLAUDE.md`
and `doc/` handbook. The published human docs are at
[sate-docs.pages.dev](https://sate-docs.pages.dev). These skills stay line-number-free so they
don't rot as the code moves.
