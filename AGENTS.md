# AGENTS.md — sakethvaishya.com

Single-page portfolio for **Saketh Vaishya**. The entire site is `index.html` (inline CSS + JS). No framework, no build step.

## Positioning

- Senior Robotics Software & Simulation Engineer at **Origin** (Nov 2025 – present); previously Techolution, SS Innovations, SegriTech, IIT Madras Touch Lab.
- The site must clearly present him as a **robotics simulation engineer**: NVIDIA Isaac Sim / Isaac Lab, digital twins, real2sim, sim-to-real, RL (PPO) + imitation learning.
- Contact on site: `sakethsandeep405@gmail.com`, github.com/Saketh-Vaishya, linkedin.com/in/saketh-vaishya. Never add a phone number.

## Rules

- **Professional, single page only.** Personal mode, mode toggle, Anywhere Door transition, mascot, doodle wall and the old skills-pill list were removed on request — do not re-add unless asked.
- **Doraemon-flavoured, animated, logo-rich — but professional.** Gadgets always map to real work.
- Pure static HTML/CSS/JS; only external dependency is Google Fonts. No libraries, trackers, CMS.
- Videos: ≤ ~5 MB, H.264, `+faststart`, `.jpg` poster, `preload="none"`, play only while visible. Files live in `assets/videos/<name>.mp4|.jpg`.
- Respect `prefers-reduced-motion` for every animation.
- Must work at **375 / 768 / 1280 px**: no horizontal scroll, finger-sized tap targets.
- Keep accessibility: aria labels, `aria-pressed`/`aria-expanded`, keyboard + Escape on the lightbox, focus outlines.

## Theme

- Neo-brutalist cartoon: cream `#FBF3E2` background with `#e7dcbf` 26px dots, navy `#16314B` 2.5px borders and hard offset shadows, accents Doraemon blue `#1F9FE0`, red `#E94B3C`, yellow `#FFC93C` (plus `--sky`, `--green`, `--pink`). Use the `:root` tokens, not raw hex.
- Fonts: Caveat (headings), Patrick Hand (casual hints), Nunito (body), Space Mono (kickers/tags/code).
- Inline SVG sprite: `#logo-mark` robot-cat (logo, buddy; favicon is a matching data-URI), simple-icons brand logos `#i-*`.

## Sections (in order)

Sticky header (progress bar, active nav) → `#hero` (typing rotator, stat counters, interactive canvas sim viewport: 2-link IK arm, particles, HUD, pauses offscreen) → `#toolbox` (logo marquees) → `#sim-lab` (4-step pipeline, terminal, What I do) → `#work` (filter chips, 12 project cards with show-more, video lightbox) → `#journey` (timeline with monogram badges, scroll-filled line) → `#why` (Why Doraemon flip cards + pocket) → `#contact`. Plus floating take-copter back-to-top buddy, scroll reveals, and a résumé button shown only if `assets/resume.pdf` exists (missing today, as is `assets/photo.jpg`).

## Privacy

`.gitignore` excludes `.env`, `CONTENT_NOTES.md` (phone number), `CLAUDE.md`, `*.pptx`, `Saketh Varma - Portfolio.html`, `generate_images.py`, `assets/*.png`, `assets/doodles/`. Never commit, force-add or copy content from them. This `AGENTS.md` is public (committed).

## Deploy

- Repo https://github.com/Saketh-Vaishya/Saketh-Vaishya.github.io (personal account Saketh-Vaishya, not the work account), GitHub Pages on `main` → sakethvaishya.com.
- Deploy = `git push` to `main`. **Never commit or push without the owner's explicit OK.**
- Auth: credential helper in `.git/config`; for `gh` use `env -u GH_TOKEN GH_CONFIG_DIR=$HOME/snap/gh/common/sakethvaishya gh ...`.

## Testing

- Open via `file://` or `python3 -m http.server` (server needed for the résumé HEAD check).
- Verify visually at 375 / 768 / 1280 px (headless Chrome screenshots work) and check the console before reporting done.
- Owner gives terse requests and expects end-to-end completion.
