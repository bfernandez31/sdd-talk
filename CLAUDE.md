# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a presentation repository for a talk on **Spec-Driven Development (SDD)**:
- **Title**: "Êtes-vous prêt à arrêter de coder ?"
- **Format**: Reveal.js presentation
- **Theme**: Catppuccin Mocha color palette
- **Demo app**: ai-board (https://ai-board-three.vercel.app/)

## Presentation Structure (45 min)

1. **Le problème** (5 min) - Vibe coding et ses limites
2. **Lancement des deux générations** (5 min) - Demo: génération SANS spec vs AVEC spec
3. **SDD: les concepts** (10 min) - spec-first, spec-anchored, spec-as-source
4. **Les patterns d'intégration** (10 min) - Structure des specs, intégration agent
5. **Analyse comparative** (10 min) - Résultats côte à côte
6. **Ouverture et Q&A** (5 min)

## SDD Concepts Reference

**Three levels of SDD**:
- **Spec-First**: Specs précèdent le code, puis sont souvent abandonnées
- **Spec-Anchored**: Specs persistent et évoluent avec la feature
- **Spec-as-Source**: La spec EST l'artefact principal, le code est généré (`// GENERATED FROM SPEC - DO NOT EDIT`)

**Spec definition**: "a structured, behavior-oriented artifact written in natural language that expresses software functionality and serves as guidance to AI coding agents"

## Catppuccin Mocha Palette

```css
/* Base */
--ctp-base: #1e1e2e;
--ctp-mantle: #181825;
--ctp-crust: #11111b;
--ctp-text: #cdd6f4;
--ctp-subtext1: #bac2de;
--ctp-subtext0: #a6adc8;
--ctp-overlay2: #9399b2;
--ctp-overlay1: #7f849c;
--ctp-overlay0: #6c7086;
--ctp-surface2: #585b70;
--ctp-surface1: #45475a;
--ctp-surface0: #313244;

/* Accents */
--ctp-rosewater: #f5e0dc;
--ctp-flamingo: #f2cdcd;
--ctp-pink: #f5c2e7;
--ctp-mauve: #cba6f7;
--ctp-red: #f38ba8;
--ctp-maroon: #eba0ac;
--ctp-peach: #fab387;
--ctp-yellow: #f9e2af;
--ctp-green: #a6e3a1;
--ctp-teal: #94e2d5;
--ctp-sky: #89dceb;
--ctp-sapphire: #74c7ec;
--ctp-blue: #89b4fa;
--ctp-lavender: #b4befe;
```

## Development Commands

```bash
# Serve presentation locally (from sdd/ directory)
npx serve .
# or
python -m http.server 8000

# Open in browser
open http://localhost:8000
```

## Reveal.js Key Features

- Use `---` for horizontal slides, `--` for vertical slides
- Speaker notes: `<aside class="notes">...</aside>`
- Fragments: `class="fragment"` for step-by-step reveals
- Code highlighting: `<pre><code data-line-numbers="1-3|5-7">` for progressive highlights
- Keyboard: arrows navigate, `S` for speaker view, `F` for fullscreen, `ESC` for overview

## Demo Strategy

The presentation runs two parallel code generations:
1. **Vibe coding**: prompt simple sans spec structurée
2. **SDD approach**: spec structurée avec acceptance criteria (GIVEN/WHEN/THEN)

Both target the same feature on ai-board. Checkpoints throughout the talk show progress.
