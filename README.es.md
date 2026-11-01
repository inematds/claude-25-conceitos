# Los 25 conceptos de Claude para quienes no programan

[![Los 25 conceptos de Claude](guia/assets/banner-es.jpg)](https://inematds.github.io/claude-25-conceitos/guia/es/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## Qué es

Esta guía explica, en lenguaje simple, los 25 recursos de Claude (el asistente de IA de Anthropic) que más aparecen en la ola de novedades de las últimas semanas. Está dirigida a quienes usan Claude en el trabajo, pero no programan: contadores, dueños de clínicas, comerciantes, docentes. Cada concepto incluye una explicación breve, un ejemplo cotidiano y el plan en el que está disponible. Al final, encontrarás una tabla de planes, tres pasos para empezar y prompts listos para copiar. No necesitas instalar nada para leerla; algunos recursos requieren el plan Pro y la aplicación de escritorio.

## 📖 Guía

Página completa: **https://inematds.github.io/claude-25-conceitos/guia/es/**

## Las 5 partes

1. **El cerebro** — modelos (Haiku, Sonnet y Opus 5.5), Fable 5.1, tokens y ventana de contexto, nivel de esfuerzo, límites y planes.
2. **Dónde usarlo** — Chat, Claude Code, Cowork, sesiones y split view, side chats, Claude Duet.
3. **Qué hace** — Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **Qué sabe de ti** — memoria, CLAUDE.md, skills, conectores, plugins, mods.
5. **Trabajar por tu cuenta** — modos de permiso, subagentes, Projects, `/goal` + extra: tareas programadas.

Además: tabla «qué incluye cada plan», «por dónde empezar: solo 3 cosas» y prompts listos (modelo de CLAUDE.md, prompt para crear una skill, 3 ejemplos de `/goal`).

Datos verificados en las páginas oficiales (claude.com, code.claude.com, support.claude.com) el 01/11/2026. Los planes y las funciones en beta cambian rápido: consulta claude.com/pricing.

## El proceso, de principio a fin

| # | Paso | Quién lo hace | Comando / dónde |
|---|---|---|---|
| 1 | Recopilar y verificar los datos en las páginas oficiales (qué está confirmado, qué difiere o qué no se encontró) | 🧠 sesión | `longrun/<data>-claude-25-conceitos/FATOS.md` (en el proyecto wifi) |
| 2 | Generar la portada y el arte de hero | ⚙️ script (Codex image_gen) | `node ~/.claude/skills/capa-inema/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Generar los 6 banners (live + grade × PT/EN/ES) | ⚙️ script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Escribir la guía en PT (25 tarjetas `data-conceito`, planes, 3 pasos, prompts, videos) | 🧠 sesión | `guia/index.html` |
| 5 | Traducir a EN y ES | 🤖 traductor central (Codex con suscripción) | `inema-traduz < pedido.txt -o guia/en/index.html` (lo mismo para `es`) |
| 6 | Verificar: 25 conceptos en cada idioma, nada de fuentes externas, sin texto en PT sobrante | ⚙️ script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publicar (commit + push; GitHub Actions publica Pages) | 🧠 sesión | `git push` → `.github/workflows/pages.yml` |
| 8 | Comprobar que esté disponible (PT/EN/ES responden 200) y tomar capturas para móvil y escritorio | ⚙️ script | `curl -sI https://inematds.github.io/claude-25-conceitos/guia/` |
| 9 | Añadir los enlaces de los videos cuando estén disponibles | 🧠 sesión | reemplazar los marcadores `<!-- VIDEO-EXPLICA -->` y `<!-- VIDEO-RTEX -->` en los 3 idiomas |

## Licencia y aviso

Contenido abierto y gratuito de [INEMA.CLUB](https://inema.club). Guía independiente; no es material oficial de Anthropic.