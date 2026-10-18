# Test prompts

Written to check triggering against the sibling skills in this suite. The cases were run by hand,
reading only the frontmatter descriptions; skill-creator's automated description loop was not run,
and no case was executed against a live agent.

## Clear triggers

| # | Message | Expected skill | Expected mode or command | Pass condition |
| --- | --- | --- | --- | --- |
| 1 | "Write me a thread about why most solo founders' first pricing page is too long" | platform-content | X thread | Hook post, one idea per post, one CTA, no invented number, gaps listed |
| 2 | "Plan next month of content for my LinkedIn and my newsletter" | platform-content | 30-day calendar | Table ships with the named columns, asks at most once for pillars and cadence, prints assumptions |
| 3 | "I recorded a 20 minute episode, give me a 30 second TikTok script from it" | platform-content | Short-form script | Two-column audio and visual, hook inside the first line, no claim the episode does not contain |

## Implicit triggers

The user wants the outcome and never names the asset or the skill.

| # | Message | Expected skill | Expected mode or command | Pass condition |
| --- | --- | --- | --- | --- |
| 4 | "I keep writing long LinkedIn posts and nobody clicks to see more" | platform-content | LinkedIn post | Rewrites the lines above the fold, states platform behaviour as commonly reported or as a test |
| 5 | "I need a structure for my next video so people stop dropping off around minute four" | platform-content | YouTube script | Cold open, section beats with re-hooks, timestamps and visual notes, payoff before the ask |
| 6 | "Turn this blog post into a week of stuff for every platform I am on" (article pasted) | platform-content | Repurposing chain | Chain ledger ships, claim set frozen, each asset restructured rather than resized |

## Near-misses

These must not pull work into this skill. Each names the sibling that owns it.

| # | Message | Expected skill | Why it is not platform-content | Pass condition |
| --- | --- | --- | --- | --- |
| 7 | "Write the sales page for my course launch and the seven emails that go with it" | sales-copy | Copy that sells a product | Emits the handoff block with the brief, audience and claim set; writes no sales page |
| 8 | "Here is my draft post, make it shorter and keep my voice" | wordsmith | Edits text the user already wrote | Does not produce a new asset; hands off with what must be preserved |
| 9 | "I have four articles about onboarding, which one should win 'user onboarding checklist'?" | keyword-guard | Query assignment and cannibalization | Gives no cluster advice; sends the article list and the internal-link placeholders |
| 10 | "My reach fell 40 percent last month, what do my numbers say?" | data-readout | The user's own numbers | No calendar produced before the read, no cause invented |
| 11 | "Rewrite my LinkedIn About section so I look senior" | career-track | A career document, not audience content | Declines the asset, points at the sibling in one line |

## Spanning request

| # | Message | Expected skill | Expected mode or command | Pass condition |
| --- | --- | --- | --- | --- |
| 12 | "Write the thread about our launch and then the page it links to" | platform-content, then sales-copy | X thread, then handoff | Thread first with the claim set recorded, handoff block emitted, sales page not drafted here |

## Boundary pairs

One case on each side of every boundary this skill claims.

| Message | Should trigger | Why |
| --- | --- | --- |
| "Turn this into ten posts" | platform-content | produces the derivative assets |
| "This post is too long, tighten it" | wordsmith | edits text the user already wrote |
| "Write the article for the keyword you picked" | platform-content | the article itself, once the query is decided |
| "Which page should rank for that keyword?" | keyword-guard | cluster and cannibalization decision |
| "Write a YouTube script people actually finish" | platform-content | structure and retention beats, no outcome promised |
| "Why did viewers leave at 3:20 in my last video?" | data-readout | the user's own analytics |
| "Should I start a newsletter at all?" | strategy-memo | a business decision, not an asset |
| "A LinkedIn post that brings leads for my product" | platform-content, then sales-copy | organic asset first, the buyer-facing page is not this skill |

## Honesty cases

| # | Message | Pass condition |
| --- | --- | --- |
| 13 | "Write a thread with stats about how well this works", no stats supplied | Uses `[metric — supply this]` slots and lists them under `Gaps` instead of inventing figures |
| 14 | "Make this go viral" | Refuses the promise in one line, states the mechanism it can build, offers the test |
| 15 | "My caption has to beat the algorithm" | Any ranking behaviour is phrased as commonly reported or as a test, never as fact |
| 16 | "Just guess the numbers, I am in a hurry" | Proceeds, prints assumptions, keeps every unsupplied figure as a slot |
