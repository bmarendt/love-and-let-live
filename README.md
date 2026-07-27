# Love and Let Live

The website for the podcast — [loveandletlive.com](https://loveandletlive.com)

*There's more that brings us together than divides us.*

## What's here

| File | What it is |
|---|---|
| `index.html` | Landing page — the credo, the episode list, and the slot the audio player drops into |
| `map.html` | The map. A rotating world of entry points, one for each tradition or worldview the show passes through, with a thread drawn between each of them |
| `404.html` | "This road isn't on the map." |
| `assets/` | Cover art, the orb, the social preview card, favicon |
| `CNAME` | Points GitHub Pages at the custom domain — don't delete it |

No build step, no framework, no dependencies. Two HTML files that run as they are. Open either one in a browser to work on it.

## Changing the map

Everything on the map is data at the top of `map.html`:

- **`NODES`** — the entry points. Add one and it appears on the map, in the picker, and in the search automatically.
- **`ROADS`** — the threads between them. Every one is a question, never a verdict. Where a fact is checkable it's stated and the open part is asked; a citation is never turned into a doubt.
- **`EPISODES`** — only what actually exists. Nothing is announced before it's known.
- **`ALIASES`** — extra search terms, so people find themselves by the word they'd actually use.

Two things are deliberate and worth not undoing:

**Radii drift.** Each marker's distance from the centre breathes on two periods that never line up. The orb at the centre is love — if any marker sat permanently nearer to it than another, the map would assert a hierarchy nobody intended.

**Only near-side markers are labelled.** That's perspective, not a ranking, and it's what lets the map keep growing without turning to mush.

## Publishing

From the folder above this one:

```
bash deploy.sh "what changed"
```

It mirrors this folder into a working clone, commits, and pushes. GitHub Pages rebuilds in about a minute. The CDN can serve a cached copy for a minute or two after that — if a change doesn't appear, wait rather than redeploying.

## Requests

The map's "request an episode" form composes an email to the show address. To move it to a proper form service, set `REQUEST_ENDPOINT` at the top of `map.html` to a Formspree or Tally endpoint; the email stays as a fallback.
