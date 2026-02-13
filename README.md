# Zero-Setup Diff

A dead-simple, zero-install tool to compare two pieces of text and see the differences highlighted word by word. No servers, no build steps — just a single HTML file you open in your browser.

## How to Use

**Use it now at <https://cgarbin.github.io/zero-setup-diff/>** — no download needed.

Or [download `index.html`](index.html) and open it locally in any browser.

1. Paste the **original** text in the left box.
2. Paste the **changed** text in the right box.
3. Click **Compare**.

Deletions appear in red with a strikethrough. Additions appear in green and bold.

## Features

- **Side-by-side view** — original text on the left, changed text on the right, each independently readable with only its relevant highlights.
- **Inline view** — toggle to a single-panel interleaved diff for quick scanning of small changes.
- **Word-level diff** — highlights individual word changes, not entire lines.
- **Strip Markdown** — optionally remove Markdown formatting before comparing.
- **Responsive** — works on desktop and mobile; panels stack vertically on narrow screens.
- **Accessible** — semantic HTML, labeled inputs, visual cues beyond color alone.
- **Swap & Clear buttons** — quickly reverse the comparison or start over.
- **Auto-recompare** — changing options or swapping texts instantly updates the diff.
- **Collapsible inputs** — inputs hide after comparing to maximize diff space; click "Edit inputs" to restore them.

## How It Works

The app uses [jsdiff](https://github.com/kpdecker/jsdiff) (`Diff.diffWords`) to compute word-level diffs. The library is loaded via CDN on first use. Results are rendered as either a side-by-side or inline view with colored highlights.

Developed with Claude Code.

## License

[MIT](LICENSE)
