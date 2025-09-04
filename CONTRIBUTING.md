# Contributing

Thanks for helping improve Mini‑CAD 2D!

## Setup
No build needed — it’s a single HTML file. Open `mini-cad.html` directly in a browser.

## Dev tips
- Use the **Test Pattern** button to ensure rendering works on your device.
- Keep to ES5‑style JavaScript for broad compatibility.
- Avoid introducing optional chaining, arrow functions, PointerEvents, ResizeObserver, etc.

## Coding standards
- Prefer small pure functions.
- Guard all drawing code with try/catch if changing transforms.
- Keep performance in mind (snaps check only nearby segments).

## Submitting changes
1. Fork the repo.
2. Create a branch: `git switch -c feat/your-feature`.
3. Commit with clear messages.
4. Open a PR with a short demo GIF/screencast if UI changes.
