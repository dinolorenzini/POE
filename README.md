# POE — Principles of Engineering

POE is a static, GitHub Pages educational workspace for Principles of Engineering. It provides interactive practice and reference material for thermodynamics and electrical circuits.

## Start here

Open **[index.html](index.html)** for the dashboard.

Main experiences:

| Page | Purpose |
|---|---|
| `index.html` | Main dashboard, navigation, local student name, performance summary, tools |
| `Thermodynamics.html` | Canonical Thermodynamics workspace with Core + Part 2 practice |
| `ThermodynamicsPt2.html` | Backwards-compatible Part 2 entry point |
| `Circuits.html` | Canonical Circuits workspace |

## How to use the site

### Thermodynamics
1. Open `Thermodynamics.html`.
2. Use **Infinite practice** for randomized practice across the Thermodynamics problem engines.
3. Use **Core** or **Part 2** when you want to focus on one question set.
4. Submit an answer in the embedded practice engine.
5. Incorrect answers reveal the existing formula/hint/worked-example guidance.
6. Use **Report** to review the current session, including submitted and expected answers.
7. Use **Learn Mode** for a guided problem-solving workflow.
8. Use **Calculator** to open the Desmos scientific calculator.

The original problem engines are intentionally kept separate internally so that their existing generators and educational content are not lost during UI work.

### Circuits
Open `Circuits.html` and use the preserved circuit trainer. The workspace wrapper provides navigation, theme control, and a new-problem action while leaving the original trainer available.

## Practice model

Practice is **not a finite course-completion meter**.

- Problems can be generated repeatedly.
- Randomized values are part of the intended experience.
- Performance is tracked separately from simply visiting a question.
- Reports are intended to explain what happened on attempts rather than only showing a completion percentage.

## Theme

The site supports light and dark themes.

- Light mode uses a restrained metallic gray palette.
- Dark mode uses a true-black base.
- Theme preference is stored in `localStorage` under `poeTheme`.

## Data and privacy

The site is static and stores local preferences/performance in the browser's `localStorage`. There is no POE backend.

Because data is local to the browser/device, clearing browser site data can remove saved local progress and preferences.

## Development

This repository is designed for GitHub Pages.

There is no build step required for the core site. HTML, CSS, and JavaScript are served directly.

### Important files

- `styles.css` — shared visual system
- `index.html` — dashboard
- `Thermodynamics.html` — Thermodynamics application shell
- `ThermodynamicsCore.html` — preserved original Thermodynamics engine
- `ThermodynamicsPart2Engine.html` — preserved original Part 2 engine
- `ThermodynamicsPt2.html` — Part 2 compatibility route
- `Circuits.html` — Circuits application shell
- `CircuitsEngine.html` — preserved original Circuits engine
- `AGENTS.md` — instructions for AI coding agents

## Rules for contributors and AI agents

Read `AGENTS.md` before making changes.

The most important rule is **preserve functionality while improving the implementation**. POE contains educational material and interactive generators; a visual redesign must not silently remove questions, formulas, references, calculators, schematics, hints, or answer checking.

Every change should be committed as a new commit. Do not rewrite repository history or force-push.

## GitHub Pages

After pushing to `main`, GitHub Pages may take a short time to deploy. If a browser appears to show an older version, hard-refresh or open the deployed page in a private window before assuming the source change failed.