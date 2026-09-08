# anki-decks

Personal Anki decks for learning programming — starting with JavaScript / TypeScript.

Decks are stored as plain-text files that can be imported directly into Anki (File → Import). Plain text keeps them git-friendly, easy to review, edit, and extend.

## Contents

- `js-ts.txt` — JavaScript `Array` methods (42 cards: all `Array.prototype` instance methods + static `Array.from / fromAsync / isArray / of`). Each card asks what a method does and gives a code example, noting whether it mutates the original array.

## File format

Each `.txt` deck uses Anki's plain-text import headers:

```
#separator:tab
#html:true
#notetype:Basic
#deck:JS/TS Programming language
#columns:Front<TAB>Back
```

- One card per line, fields separated by a single **tab**.
- HTML is enabled, so cards use `<code>`, `<b>`, `<br>`, `<pre>` for formatting.
- No raw newlines/tabs inside a field — use `<br>` for line breaks.

## How to use

1. Open Anki → File → Import.
2. Select e.g. `js-ts.txt`.
3. Confirm: Separator = Tab, Notetype = Basic, Deck matches header.
4. Study. Re-import the same file to update (Anki matches on first field).

## How to add cards

Append one line per card to the deck file:

```
Front text<TAB>Back text with <br> for newlines
```

Example:

```
What does <code>Array.prototype.map()</code> do?<TAB>Creates a <b>new array</b> ...<br><br><pre><code>[1,2].map(n =&gt; n*2)</code></pre>
```

Keep cards small (one method/concept each), include a minimal runnable example, and state mutate vs. non-mutate behavior where relevant.
