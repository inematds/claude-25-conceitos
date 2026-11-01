# Os 25 conceitos do Claude para quem não programa

[![Os 25 conceitos do Claude](guia/assets/banner.jpg)](https://inematds.github.io/claude-25-conceitos/guia/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## O que é

Este guia explica, em português simples, os 25 recursos do Claude (o assistente de IA da Anthropic) que mais aparecem na leva de novidades das últimas semanas. É para quem usa o Claude no trabalho mas não programa: contador, dono de clínica, lojista, professor. Cada conceito tem uma explicação curta, um exemplo do dia a dia e o plano em que está disponível. No fim, uma tabela de planos, três passos para começar e prompts prontos para copiar. Para ler não precisa instalar nada; alguns recursos pedem o plano Pro e o app de computador.

## 📖 Guia

Página completa: **https://inematds.github.io/claude-25-conceitos/guia/**

## As 5 partes

1. **O cérebro** — modelos (Haiku, Sonnet e Opus 5.5), Fable 5.1, tokens e janela de contexto, nível de esforço, limites e planos.
2. **Onde usar** — Chat, Claude Code, Cowork, sessões e split view, side chats, Claude Duet.
3. **O que ele faz** — Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **O que ele sabe de você** — memória, CLAUDE.md, skills, conectores, plugins, mods.
5. **Trabalhar sozinho** — modos de permissão, subagentes, Projects, `/goal` + bônus: tarefas agendadas.

Mais: tabela "qual plano tem o quê", "por onde começar: só 3 coisas" e prompts prontos (modelo de CLAUDE.md, prompt para criar skill, 3 exemplos de `/goal`).

Fatos conferidos nas páginas oficiais (claude.com, code.claude.com, support.claude.com) em 01/11/2026. Planos e recursos em beta mudam rápido: confira em claude.com/pricing.

## O processo, do início ao fim

| # | Passo | Quem faz | Comando / onde |
|---|---|---|---|
| 1 | Levantar e conferir os fatos nas páginas oficiais (o que é confirmado, divergente ou não achado) | 🧠 sessão | `longrun/<data>-claude-25-conceitos/FATOS.md` (no projeto wifi) |
| 2 | Gerar a capa e a arte da hero | ⚙️ script (Codex image_gen) | `node ~/.claude/skills/capa-inema/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Gerar os 6 banners (live + grade × PT/EN/ES) | ⚙️ script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Escrever o guia em PT (25 cartões `data-conceito`, planos, 3 passos, prompts, vídeos) | 🧠 sessão | `guia/index.html` |
| 5 | Traduzir para EN e ES | 🤖 tradutor central (Codex pela assinatura) | `inema-traduz < pedido.txt -o guia/en/index.html` (idem `es`) |
| 6 | Verificar: 25 conceitos em cada idioma, nada de fonte externa, sem texto PT sobrando | ⚙️ script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publicar (commit + push; o GitHub Actions sobe o Pages) | 🧠 sessão | `git push` → `.github/workflows/pages.yml` |
| 8 | Conferir no ar (PT/EN/ES respondem 200) e print mobile/desktop | ⚙️ script | `curl -sI https://inematds.github.io/claude-25-conceitos/guia/` |
| 9 | Pôr os links dos vídeos quando saírem | 🧠 sessão | trocar os marcadores `<!-- VIDEO-EXPLICA -->` e `<!-- VIDEO-RTEX -->` nos 3 idiomas |

## Licença e aviso

Conteúdo aberto e gratuito do [INEMA.CLUB](https://inema.club). Guia independente; não é material oficial da Anthropic.
