# Side-by-Side Visual Text Diff

A dead-simple, zero-install tool to compare two pieces of text and see the differences highlighted word by word. No servers, no build steps — just a single HTML file you open in your browser.

## How to Use

1. [Download `index.html`](index.html) (or clone this repo).
2. Open it in any modern browser (double-click the file).
3. Paste the **original** text in the left box.
4. Paste the **changed** text in the right box.
5. Click **Compare**.

Deletions appear in red with a strikethrough. Additions appear in green and bold.

## Features

- **Side-by-side view** — original text on the left, changed text on the right, each independently readable with only its relevant highlights.
- **Inline view** — toggle to a single-panel interleaved diff for quick scanning of small changes.
- **Word-level diff** — highlights individual word changes, not entire lines.
- **Strip Markdown** — optionally remove Markdown formatting before comparing.
- **Responsive** — works on desktop and mobile; panels stack vertically on narrow screens.
- **Accessible** — semantic HTML, labeled inputs, visual cues beyond color alone.
- **Swap & Clear buttons** — quickly reverse the comparison or start over.

## How It Works

The app uses [jsdiff](https://github.com/kpdecker/jsdiff) (`Diff.diffWords`) to compute word-level diffs. The library is loaded via CDN on first use. Results are rendered as either a side-by-side or inline view with colored highlights.

## License

[MIT](LICENSE)
