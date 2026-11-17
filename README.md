# Phase Transition

AI-driven discovery, acceleration, risk and the AI bubble, graded on evidence. A sister site to Longevity News and Surety Market Intelligence.

## Deploy (GitHub Pages)
1. Create a repo named `PhaseTransition`.
2. Commit every file in this folder to the root of `main`.
3. Go to Settings → Pages → Deploy from branch → `main` / root.
4. The site will be live at `https://richiebuchanan.github.io/PhaseTransition/`.

## Files
| File | Page |
|---|---|
| `index.html` | Discovery Feed |
| `baseline.html` | State of the Frontier (versioned summary) |
| `curve.html` | The Curve (forecast tracker, METR time horizons, acceleration signals) |
| `risk.html` | Risk Watch |
| `bubble.html` | Bubble Watch |
| `voices.html` | Voices |
| `media.html` | Podcasts & Video |
| `overview.html` | About |
| `admin.html` | Password-gated intake (same password as the sister sites) |
| (none) | Each page is self-contained (styles and scripts inlined), like the sister sites |
| `daily-task-prompt.md` | Prompt for the daily scheduled task |

## Backend
- Supabase project `acxdvzcohjayvmqdaoke`, tables `phase_*`. All tables have public read access; the two queue tables have no public access.
- Edge function `phase-queue-submit` handles admin intake. It is password-gated and uses the service role.

## Cross-links
- Nav and footer link to Longevity News; About links to both sister sites.
- `phase_discoveries.longevity_article_id` adds an "Also on Longevity News" badge and links to `LongevityNews/index.html#article-{id}`.
- Suggested reverse link on Longevity News: add `<a class="sister" href="https://richiebuchanan.github.io/PhaseTransition/" target="_blank" rel="noopener">Phase Transition ↗</a>` to its nav.
