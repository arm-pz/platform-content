# Calendar and repurposing

Two jobs: map a period of content before any of it is written, and turn one finished piece into
per-platform assets. Both are planning artifacts, so neither may invent a fact to fill a cell.

## 30-day calendar

### Collect first

Ask once, in one message, for whatever is missing from this list:

- Platforms the user actually posts on, and the cadence they can keep without a team.
- Pillars: three to five recurring themes that map to what the user sells, knows or has done. Use
  the user's own words for them, and refuse a pillar the user cannot speak to from material.
- Goal weighting: which pillar serves which goal (audience growth, sign-ups, inbound enquiries).
- Fixed anchors: launches, dates, events, a season, a posting blackout.
- Anything already written that the calendar can reuse.

If the user gives none of it and says go, build the calendar on stated assumptions and print them
above the table.

### The table

One asset per row, one row per day. Keep the columns; they are what makes the plan reviewable.

```
Day | Platform | Pillar | Mode | Hook type | Working hook | CTA | Source | Status
```

- `Mode` uses the names in SKILL.md so a row can be written on request.
- `Hook type` comes from the hook list in `references/formats.md`. It shows the mix at a glance.
- `Source` names the origin piece when the row is a derivative, otherwise `new`.
- `Status` is `planned`, `drafted`, `scheduled` or `published`, and only moves on evidence.

### Filling the days without invention

1. Lay the pillars across the period in rotation so no theme disappears for a week.
2. Alternate formats within a platform: a thread, then a single post, then something visual-led.
3. Put the platform's strongest format where the pillar is strongest. Long video and blog where the
   user has depth, short-form and captions where they have a repeatable point, threads and LinkedIn
   posts where they have an opinion.
4. Book the heavy assets first (video, article, episode) and fill the rest with derivatives of them,
   so `Source` is never empty by accident.
5. Reserve a small number of rows as reactive slots rather than promising 30 finished assets the
   user cannot verify.
6. Add a review checkpoint a fortnight in: what shipped, what the user can see in their own
   dashboard, what gets cut. Hand that read to `data-readout` if the user brings numbers.

### Cadence sanity

Reduce the plan rather than the quality when the cadence exceeds what the user can do. Say plainly
which rows were dropped and why. A calendar the user cannot execute is a list, not a plan.

## Repurposing chain

One source piece, several platform-native assets. The unit of work is the claim, not the paragraph.

### Chain rules

- **Extract first.** From the source, list the claims, the examples, the steps and any figures the
  user supplied. That list is the only source of facts for every derivative.
- **The claim set is frozen.** No derivative may add a fact, a number or a promise the source lacks.
  If a platform needs something the source does not have, write `[evidence — supply this]` and name
  it under `Gaps`.
- **Restructure, do not resize.** Each asset is rebuilt in its own platform's shape from
  `references/formats.md`. A thread pasted into LinkedIn, or a blog's intro used as a caption, fails
  the chain even when the words are correct.
- **New hook per platform.** Pick a different hook type where the audience differs, and keep the
  promise identical.
- **One CTA per asset**, appropriate to the platform, and the same destination where the goal is
  shared.
- **Label the lineage.** Each asset records its source and the claim IDs it carries, so the user can
  see where a line came from.

### Standard chains

Long video or podcast episode:
```
source → episode/article summary → X thread (one point per claim)
       → LinkedIn post (the takeaway, personal framing only if the user supplied a detail)
       → two to four short-form scripts (one claim each)
       → Instagram caption per clip [clip — supply this]
       → newsletter section (the argument, in full)
       → blog article (the structure, with keyword-guard deciding its query)
```

Blog article:
```
source → X thread (count stack from the H2 list)
       → LinkedIn post (the contrarian or problem-first hook, one section only)
       → newsletter issue (the piece the article cannot be, plus the opt-in)
       → short-form script (the single most repeatable step)
       → podcast outline (the questions the article answered badly in writing)
```

Newsletter issue:
```
source → X thread → LinkedIn post → short-form script → caption set → article skeleton
       (article hands its query choice to keyword-guard)
```

Small source (a stat the user supplied, a customer line, an internal doc):
```
source → one post per platform, single-claim, no chain beyond a thread
```

Choose the chain by what the source actually contains. A 400-word note does not yield a video script;
say so and offer the two assets it does yield.

### Chain ledger

Ship the chain with this table so the user can work down it:

```
Asset | Platform | Mode | Hook type | Claims carried | CTA | Needs from user
```

`Needs from user` holds the slots: links, clips, footage, figures, names. Nothing counts as finished
while it has an entry there.

### Order of work

1. Publish or record the source.
2. Derive the assets that need it live (a thread quoting the article, a caption pointing at the clip).
3. Space the rest across the calendar rows, filling `Source` so the plan shows its own dependencies.
4. Re-read the whole set before handing it over: same facts, different structures, one CTA each.
