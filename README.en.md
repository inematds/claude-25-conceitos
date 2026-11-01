# Claude’s 25 Concepts for People Who Don’t Code

[![Claude’s 25 Concepts](guia/assets/banner-en.jpg)](https://inematds.github.io/claude-25-conceitos/guia/en/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## What it is

This guide explains, in plain language, the 25 Claude features (Anthropic’s AI assistant) that have appeared most often in the wave of announcements over the past few weeks. It is for people who use Claude at work but don’t code: accountants, clinic owners, shopkeepers, teachers. Each concept has a short explanation, an everyday example, and the plan that includes it. At the end, there’s a plan comparison table, three steps to get started, and ready-to-copy prompts. You don’t need to install anything to read it; some features require the Pro plan and the desktop app.

## 📖 Guide

Full page: **https://inematds.github.io/claude-25-conceitos/guia/en/**

## The 5 parts

1. **The brain** — models (Haiku, Sonnet, and Opus 5.5), Fable 5.1, tokens and context window, effort level, limits, and plans.
2. **Where to use it** — Chat, Claude Code, Cowork, sessions and split view, side chats, Claude Duet.
3. **What it does** — Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **What it knows about you** — memory, CLAUDE.md, skills, connectors, plugins, mods.
5. **Working on its own** — permission modes, subagents, Projects, `/goal` + bonus: scheduled tasks.

Also included: a “which plan has what” table, “where to start: just 3 things,” and ready-to-use prompts (a CLAUDE.md template, a prompt to create a skill, 3 `/goal` examples).

Facts checked against official pages (claude.com, code.claude.com, support.claude.com) on 11/01/2026. Plans and beta features change quickly: check claude.com/pricing.

## The process, from start to finish

| # | Step | Who does it | Command / where |
|---|---|---|---|
| 1 | Gather and verify facts on official pages (what’s confirmed, conflicting, or not found) | 🧠 session | `longrun/<data>-claude-25-conceitos/FATOS.md` (in the wifi project) |
| 2 | Generate the cover and hero artwork | ⚙️ script (Codex image_gen) | `node ~/.claude/skills/capa-inema/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Generate the 6 banners (live + grid × PT/EN/ES) | ⚙️ script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Write the guide in PT (25 `data-conceito` cards, plans, 3 steps, prompts, videos) | 🧠 session | `guia/index.html` |
| 5 | Translate into EN and ES | 🤖 central translator (Codex by subscription) | `inema-traduz < pedido.txt -o guia/en/index.html` (same for `es`) |
| 6 | Verify: 25 concepts in each language, no external fonts, no leftover PT text | ⚙️ script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publish (commit + push; GitHub Actions publishes Pages) | 🧠 session | `git push` → `.github/workflows/pages.yml` |
| 8 | Check that it’s live (PT/EN/ES return 200) and capture mobile/desktop screenshots | ⚙️ script | `curl -sI https://inematds.github.io/claude-25-conceitos/guia/` |
| 9 | Add video links when they’re released | 🧠 session | replace the `<!-- VIDEO-EXPLICA -->` and `<!-- VIDEO-RTEX -->` markers in all 3 languages |

## License and notice

Open, free content from [INEMA.CLUB](https://inema.club). Independent guide; not official Anthropic material.