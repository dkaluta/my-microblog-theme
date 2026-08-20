# my-microblog-theme

A [Micro.blog](https://micro.blog) theme for [blog.dkaluta.com](https://blog.dkaluta.com),
restyled to match the terminal aesthetic of [dkaluta.com](https://dkaluta.com)
([source](https://github.com/dkaluta/dkaluta.github.io)).

**This is a fork of the [Sumo Theme](https://github.com/MattSLangford/Sumo-Theme)
by [Matt Langford](https://mattlangford.com)** — all of Sumo's structure,
Microhooks, and plugin support are retained. If you like what Sumo provides,
please consider [supporting Matt's work](https://sumo.micro.blog).

## What the fork changes

- **Terminal look**: the whole page renders inside a tty window (dot bar +
  title), strict 16-color ANSI palette (`--color0`…`--color15` + `--bg`/`--fg`),
  monospace type, prompt-styled header (`~$`), squared-off controls.
- **Auto light/dark**: pure `prefers-color-scheme` media queries flip between
  Tomorrow Night (dark) and Tomorrow (light) — same palette and behavior as
  the main site — with `color-scheme` and `theme-color` keeping the browser
  chrome in step.
- **RTL / Hebrew support**: content containers carry `dir="auto"`, paragraphs
  resolve their own direction (`unicode-bidi: plaintext`) so mixed
  Hebrew/English posts read naturally, logical CSS properties flip padding
  and blockquote borders, and a Hebrew translation file (`i18n/he.json`) is
  included. Window chrome and dates stay LTR by design.
- **Fonts**: Latin text renders in Source Code Pro; Hebrew falls through to
  Cascadia Code (which ships Hebrew glyphs), both loaded from Google Fonts.
- **ISO dates** (`2006-01-02`) by default; override with the standard
  `dateFormatLong` / `dateFormatShort` params.
- **Follow button** (`./follow` in the header): tries to open the visitor's
  newsreader via the `feed://` scheme; when none answers, the panel explains
  what a newsreader is and suggests free ones per platform (NetNewsWire,
  Feeder, RSS Guard) plus the JSON Feed URL. Localized, and usable
  without JS (`<details>` + a plain `feed://` link).
- Targets **Hugo 0.91** (the Micro.blog engine version).

## Credits & license

Sumo Theme was created by [Matt Langford](https://mattlangford.com); this fork
is by [David Kaluta](https://dkaluta.com). MIT licensed — see [LICENSE](LICENSE)
(original copyright retained).

### Support the original

Help fund Matt's ongoing work on Tiny, Sumo, and Bayou:

- <a href="https://donate.stripe.com/7sI28l5dCdvA0Mg6oq">One-Time (Any Amount)</a>
- <a href="https://donate.stripe.com/dR6aER8pO2QWdz29AD">Monthly $5</a>
