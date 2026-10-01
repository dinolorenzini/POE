# POE Agent Guide

## Purpose
POE is a GitHub Pages educational site for Principles of Engineering. It contains interactive practice for thermodynamics and circuits, plus formulas, references, schematics, calculators, and learning aids.

This file is the source of truth for AI coding agents working in this repository.

## Non-negotiable rules

1. **Preserve existing functionality.** Do not replace a large page with a simplified demo just to make the UI easier to edit.
2. **Inspect before editing.** Fetch the complete current file from `main` before modifying it. Do not reconstruct large files from snippets.
3. **Never rewrite history.** Never force-push, reset, or overwrite an existing commit. Every change must be a new commit.
4. **Verify after editing.** Re-fetch changed files and check that the intended code exists before reporting completion.
5. **No `alert()`.** Use inline feedback, drawers, modals, toasts, or other UI already present.
6. **No destructive cleanup.** Before removing old code/content, verify that it is genuinely unused and that its functionality is preserved elsewhere.
7. **GitHub Pages compatibility.** This is a static site. Do not introduce a server dependency unless explicitly requested.
8. **Keep external dependencies deliberate.** If using a CDN, pin the version where practical and make sure the site still works on GitHub Pages.
9. **Use real icons.** The UI uses Lucide icons where icons are appropriate; do not replace them with emoji.
10. **Test the user path.** Buttons, navigation, theme switching, calculators, practice generation, answer checking, reports, and links must actually work.

## UI direction

The target visual language is:
- professional educational engineering software
- flat metallic grayscale
- true-black dark mode
- restrained borders and shadows
- small/medium corner radii
- real typography
- Lucide icons
- no blue accent system
- no glassmorphism
- no excessive gradients
- no giant rounded cards
- no generic AI-dashboard appearance

Use the existing CSS variables and components where possible instead of creating a second unrelated design system.

## Thermodynamics architecture

- `Thermodynamics.html` is the canonical Thermodynamics entry point.
- `ThermodynamicsPt2.html` is a compatibility entry point that routes to the canonical page's Part 2 mode.
- `ThermodynamicsCore.html` preserves the original core problem engine.
- `ThermodynamicsPart2Engine.html` preserves the original Part 2 problem engine.
- Do not delete either engine unless all of its problem generators, formulas, references, hints, examples, and other functionality have been migrated and verified.
- Practice is intended to be unlimited/randomized. A score represents performance, not completion.
- Reports should expose useful attempt information such as submitted answer, expected answer, topic, correctness, and attempt count.
- Preserve MathJax, Desmos, formulas, references, schematics, hints, worked examples, and unit checking.

## Circuits architecture

- `Circuits.html` is the user-facing circuit workspace.
- `CircuitsEngine.html` preserves the original circuit trainer.
- The original multi-level circuit functionality must remain available.

## Editing workflow

1. Read `AGENTS.md`.
2. Inspect the relevant existing files and their current SHAs.
3. Make the smallest complete change that satisfies the request.
4. Create/update files on `main` using a new commit.
5. Re-fetch the changed files.
6. Search for regressions such as accidental `alert(`, removed key IDs/functions, broken links, or duplicate obsolete entry points.
7. Report the commit SHA(s) and exactly what was changed.

## Commit discipline

Use focused commit messages, for example:
- `Add unified thermodynamics report`
- `Refine circuit workspace navigation`
- `Fix dark-mode persistence`

Do not squash or rewrite prior work unless explicitly instructed by the repository owner.

## Content preservation checklist

Before considering a redesign complete, verify:
- [ ] all original problem generators remain
- [ ] all question sets remain
- [ ] formulas remain
- [ ] references remain
- [ ] Desmos remains
- [ ] schematics/visualizations remain
- [ ] hints remain
- [ ] worked examples remain
- [ ] randomized generation remains
- [ ] answer/unit checking remains
- [ ] Learn Mode works
- [ ] report works
- [ ] dark/light mode works
- [ ] navigation works
- [ ] no `alert()`
- [ ] no broken primary buttons
