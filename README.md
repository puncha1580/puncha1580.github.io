# Puneet — Portfolio

A static HTML/CSS/JavaScript portfolio intended to be reviewed locally before publication to GitHub Pages.

## Structure

```text
Puneet-Portfolio/
├── index.html              # Single-page portfolio (Tailwind CDN, dark-mode toggle)
├── README.md
├── coming-soon.html        # Placeholder for assets still pending
├── Puneet-Portfolio/       # Legacy redirect shim -> https://puncha1580.github.io/
│   └── index.html
└── assets/
    ├── cv/                 # Puneet_CV.pdf
    ├── documents/          # PDFs (fuel dispenser manual, lesson plans)
    ├── games/              # Standalone HTML games (POSH Guardian, German Learning)
    ├── learning/           # VILT modules, microlearning, CBTs
    └── images/
```

Note: the earlier multi-page layout (about/, cv/, technical-writing/, etc.) was never implemented. The live site is a single monolithic index.html. Navigation is in-page anchor links (#hero, #learnings, #simulator, #articles, #timeline, #contact).

## Preview locally

Open `index.html` in a browser. For a more reliable local preview, use VS Code with a local server extension. Navigation links use explicit `index.html` paths to avoid directory-listing behaviour in some local preview setups.

## Asset files intentionally pending

Until the actual files are added, asset links open `coming-soon.html` instead of a broken page. Each temporary link stores its intended destination in a `data-asset-target` attribute. When you add an asset, restore that link's `href` to the destination shown in `data-asset-target`:

- `assets/documents/Fuel_Dispenser_Manual.pdf`
- `assets/learning/Grade7_English_VILT.html`
- `assets/learning/Grade7_English_Lesson_Plan.pdf`
- `assets/games/German_Learning_Game.html`
- `assets/presentations/QDD_Micro_Presentation.html`
- `assets/cv/Puneet_CV.pdf`

Keep these names consistent, or update the corresponding links when you add the actual files. You can add more assets to these folders later.

## Design and implementation notes

- Plain HTML, CSS, and a small optional JavaScript file; no framework or build step.
- Responsive layouts for desktop and mobile.
- Semantic landmarks, skip links, and visible keyboard focus styles.
- Reduced-motion preference is respected.
- Portfolio copy distinguishes historical sample work, concepts in development, and future additions.
- No fabricated email address or social profile has been inserted. Add the preferred contact details before publication.

## Before publishing

1. Add the final assets and confirm each asset link.
2. Add the contact details and profile links you want public.
3. Review every project description for accuracy.
4. Test all links at desktop and mobile widths.
5. Publish the folder to the intended GitHub repository only after review.
