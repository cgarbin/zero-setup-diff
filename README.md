# Side-by-Side Visual Text Diff

A dead-simple, zero-install tool to compare two pieces of text and see the differences highlighted word by word. No servers, no dependencies, no build steps — just a single HTML file you open in your browser.

## How to Use

1. [Download `index.html`](index.html) (or clone this repo).
2. Open it in any modern browser (double-click the file).
3. Paste the **original** text in the left box.
4. Paste the **changed** text in the right box.
5. Click **Compare**.

Deletions appear in red with a strikethrough. Additions appear in green and bold.

## Features

- **Word-level diff** — highlights individual word changes, not entire lines.
- **Fully self-contained** — a single HTML file with no external dependencies.
- **Works offline** — no network requests, no CDN, no tracking.
- **Responsive** — works on desktop and mobile.
- **Accessible** — semantic HTML, labeled inputs, visual cues beyond color alone.
- **Swap & Clear buttons** — quickly reverse the comparison or start over.

## How It Works

The app uses a Longest Common Subsequence (LCS) algorithm to compare word tokens from both texts. It classifies each word as kept, deleted, or inserted, then renders the result as an inline diff with colored highlights.

## License

[MIT](LICENSE)
