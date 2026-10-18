# platform-content

An agent skill that writes platform-native audience content from a brief. Give it the platform, the
niche, the audience and the goal, and it produces the asset: an X thread, a LinkedIn post, a YouTube
or TikTok script, an Instagram caption, a newsletter issue, a blog article, a podcast outline, a
30-day calendar, or one finished piece broken into derivatives for every platform. Each asset comes
with a hook, a body and one call to action, plus a written list of the figures it did not have.

Install: `npx skills add arm-pz/platform-content --skill platform-content`

Ask it things like:

- "Write me a thread about why most first pricing pages are too long."
- "A YouTube script people actually finish, for a 10 minute video on schema migrations."
- "Turn this blog post into a week of content for LinkedIn, X and Instagram."
- "Plan 30 days of content for a book editor whose audience is first-time novelists."

## What you get

| Mode | Output |
|---|---|
| X thread | Hook post, one-idea value posts, recap, closing call to action |
| LinkedIn post | Lines above the fold, short-line body, takeaway, call to action plus a comment variant to test |
| YouTube script | Cold open, section beats with re-hooks, payoff, end-screen ask, timestamps and visual notes |
| Short-form script | Two-column audio and visual script with a hook in the first line and a loop or ask at the end |
| Instagram caption | Opening-line options, caption body, one call to action, hashtag and link slots |
| Newsletter issue | Subject options, preview text, opening, sections, one call to action, postscript |
| Blog article | Answer-first intro, H2 skeleton, body with evidence slots, internal-link placeholder list, opt-in block |
| Podcast outline | Cold open, timed segment map, ordered question bank, written transitions, ad and outro slots |
| 30-day calendar | Day-by-day table: platform, pillar, mode, hook type, working hook, call to action, source, status |
| Repurposing chain | Per-platform derivatives plus a chain ledger showing which claims each asset carries and what is still missing |

Every asset carries an `Assumptions` line and a `Gaps` line. Anything the skill could not get from
the brief or a fetched source stays as a labelled slot.

## Not for

Copy that sells a product: sales pages, ads, launch email sequences, landing pages and VSL scripts
belong to `sales-copy`. Rewriting text you already wrote belongs to `wordsmith`. SEO topic clusters,
keyword assignment and cannibalization decisions belong to `keyword-guard`; this skill writes the
article and hands the query choice over. Career documents belong to `career-track`. Deciding whether
a channel is worth the investment is a `strategy-memo`, and reading your own analytics back to you is
`data-readout`.

It also will not promise performance. No "viral", no guaranteed reach, no asserted ranking mechanic.
Platform behaviour is phrased as commonly reported or as a test, and each call to action ships with
the comparison that would tell you whether it worked.

## Install

```
npx skills add arm-pz/platform-content --skill platform-content
```

Or copy `skills/platform-content/` into your agent's skills directory (`.claude/skills/`,
`.agents/skills/`, `.cursor/skills/` or `.qoder/skills/`). With Claude Code plugins,
`.claude-plugin/plugin.json` makes the repo installable as a plugin; add it to your marketplace repo
as an entry pointing at `arm-pz/platform-content`.

## Structure

```
platform-content/
├── README.md
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── platform-content/
│       ├── SKILL.md                     # intake, modes, output format, quality bar, handoffs
│       └── references/
│           ├── formats.md               # per-platform structure, hook types, retention beats, CTA patterns
│           └── calendar-repurposing.md  # calendar columns, filling rules, repurposing chains and ledger
└── tests/
    └── test-prompts.md                  # triggers, near-misses and boundary pairs against the siblings
```

## Build notes

SPEC GAP: the suite design names a third reference, `quality-bar.md`, while the build brief lists two; the honesty and craft rules live in the Quality bar section of `SKILL.md` instead, so nothing is duplicated or left to fetch.

SPEC GAP: section 1 of the design says "the nine listed formats plus" the calendar and the chain, but the source list carries ten items with eight formats in it. The modes table follows the source list: one row per capability, with the YouTube script and the short-form script kept apart.

## Licence

MIT. See `LICENSE`.
