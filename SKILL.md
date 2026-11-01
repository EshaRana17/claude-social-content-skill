---
name: social-content
description: Turns long-form material into platform-native social media posts and plans what to publish. Repurposes a blog post, video transcript or podcast notes into an X thread, LinkedIn post, Instagram carousel (slide-by-slide copy plus caption), TikTok/Reels/Shorts script and Threads or Bluesky post; writes hooks and headlines across named patterns; builds a 30-day content calendar as CSV; extracts a brand voice guide from sample posts; and reviews drafts for hook, clarity, scannability, CTA and accessibility. Use when the user mentions social media, an X or Twitter thread, a LinkedIn post, an Instagram carousel, a TikTok, Reels or Shorts script, a content calendar, hooks, captions, repurposing content, or brand voice. Follows honest-marketing rules - no fake engagement, fake reviews or invented statistics, and clear disclosure of sponsorships and affiliations.
license: MIT
---

# Social Content Studio

A working method for creators, founders and small brands who need to publish
consistently without sounding like a template. Five workflows share one set of
rules: write for the platform, keep the claims true, and make every post
readable by everyone.

## How to use this skill

1. Identify which workflow the request needs (it may be more than one).
2. Collect the inputs listed for that workflow. Ask only for what is missing and
   cannot be reasonably inferred; otherwise state the assumption and proceed.
3. Read the matching reference file before producing output:

| Need | Read |
|------|------|
| Character limits, formats, platform norms | `references/platforms.md` |
| Hook and headline patterns | `references/hooks.md` |
| Turning one source into many posts | `references/repurposing.md` |
| 30-day plans and cadence | `references/calendar.md` |
| Building and applying a voice guide | `references/voice.md` |
| Disclosure, claims, platform manipulation rules | `references/ethics.md` |

4. Run the ethics check (below) on everything before handing it over.
5. Label every output with the platform and a character count for anything
   near a limit.

If a voice guide exists in the conversation or the user's files, apply it to
every workflow. If none exists, write in a plain, specific, confident register
and say so.

## Global rules

- **Source fidelity.** Every claim, number, quote and result in a post must
  come from the user's source material or from the user. Never invent
  statistics, customer quotes, case studies, follower counts or outcomes. If a
  post would be stronger with a number the source lacks, write a placeholder
  like `[ADD: % of users who finished onboarding]` and flag it.
- **Platform-native, not copy-paste.** The same idea gets a different shape on
  each platform (see `references/platforms.md`). Never paste a LinkedIn post
  into X with the end trimmed off.
- **Limits are hard constraints.** Stay under each platform's limit with a
  safety margin. Treat limits in `references/platforms.md` as last verified on
  the date shown; if the user reports a different limit, use theirs.
- **Accessibility by default.** Write alt text for every image or slide,
  CamelCase multi-word hashtags (`#SmallBusinessTips`), avoid walls of emoji or
  stylised Unicode "fonts" (screen readers read them letter by letter), and add
  on-screen captions to every video script.
- **No emojis unless the user's voice guide uses them.** If it does, match its
  frequency, never exceed it.
- **One idea per post.** If the source has five ideas, that is five posts or a
  thread, not one crowded post.

## Workflow 1: Repurpose one piece

**Inputs:** the source (text, transcript, notes or link content the user
pasted), target platforms (default: all five below), audience, goal (reach,
clicks, replies, sign-ups), any link or CTA, voice guide if present.

**Steps:**

1. Extract an "idea inventory" from the source: the core thesis, 3-7 supporting
   points, concrete specifics (numbers, examples, quotes, steps) and the single
   most surprising line. Note what is the user's own data versus cited data.
2. Pick the angle per platform (see the matrix in `references/repurposing.md`).
   Not every point belongs on every platform.
3. Draft each format:
   - **X thread:** hook post that stands alone, 4-10 posts, one point each,
     each post under the free-tier limit, link in the final post or a reply.
   - **LinkedIn post:** first two lines carry the hook before the "see more"
     fold, short paragraphs, one takeaway, a question or clear CTA at the end,
     3 or fewer hashtags.
   - **Instagram carousel:** slide-by-slide table (slide number, headline,
     body text, visual note, alt text), a cover slide that promises the payoff,
     a final slide with the CTA, plus caption and up to the hashtag cap.
   - **Short-video script (TikTok, Reels, Shorts):** hook (first 1-3 seconds,
     spoken and on screen), beats with timestamps, on-screen text per beat,
     B-roll or visual notes, CTA, and a caption.
   - **Threads / Bluesky post:** conversational, single post under the
     Bluesky limit so one draft works for both, optional reply-chain for
     extra detail.
4. Check every draft against limits, the voice guide and the ethics check.
5. Deliver in the output format below, with a short note on what was left out
   and why.

**Output format:** one Markdown section per platform, headed with the platform
name and character count. Carousels and scripts as tables. End with "Assumptions
and placeholders" listing anything the user must fill in or confirm.

Full templates, a worked example and the angle matrix are in
`references/repurposing.md`.

## Workflow 2: Hooks and headlines

**Inputs:** topic or draft, platform, audience, what the content actually
delivers.

**Steps:**

1. Write down the content's real payoff in one sentence. Every hook must be
   honestly paid off by that sentence.
2. Generate options across the five named patterns (at least two each unless
   the user asks for fewer):
   - **Curiosity gap** - open a specific question the content answers.
   - **Contrarian** - challenge a common belief the content actually argues
     against.
   - **Specific result** - lead with a concrete, true outcome and timeframe.
   - **Story open** - drop the reader into a moment with tension.
   - **List promise** - commit to a countable, delivered set of items.
3. For each option give: the hook, the pattern, why it works for this audience
   (one line), and a "payoff check" naming where in the content it is paid off.
4. Recommend the top two with reasons, and flag any option that drifts toward
   clickbait.
5. Reject or rewrite anything that promises more than the content delivers,
   implies a result the user has not had, or manufactures urgency.

Pattern formulas, strength tests and the clickbait test are in
`references/hooks.md`.

## Workflow 3: 30-day content calendar

**Inputs:** goal(s) with a measurable target if the user has one, 3-5 content
pillars (or derive them from the user's offer and audience), platforms,
realistic weekly capacity (hours or posts), start date, key dates (launches,
events, holidays relevant to the audience), existing long-form assets.

**Steps:**

1. Confirm capacity first. A plan the user cannot sustain is a bad plan; size
   cadence to capacity, not to an ideal.
2. Assign pillar weights (for example 40/30/20/10) tied to the goal.
3. Choose a format mix per platform (see `references/calendar.md`), anchored
   on one or two "hero" long-form pieces that get repurposed across the month.
4. Lay out 30 days: date, platform, pillar, format, working title/hook,
   CTA, asset needed, status. Leave at least one buffer slot per week.
5. Add a weekly review step: which three metrics to check and what change each
   result should trigger.
6. Output as a Markdown table and as CSV using the exact header of
   `assets/content_calendar.csv`. Dates in ISO format (YYYY-MM-DD).

Cadence guidance, pillar examples and the review loop are in
`references/calendar.md`.

## Workflow 4: Brand voice

**Inputs:** 3-5 sample posts or paragraphs the user considers on-brand
(their own writing, not someone else's), plus optional "never sound like"
examples.

**Steps:**

1. If fewer than three samples are provided, say the guide will be
   provisional and proceed with what exists.
2. Analyse the samples across the dimensions in `references/voice.md`: tone
   sliders, sentence rhythm (average length, variation, fragments),
   vocabulary (signature words, banned words, jargon level), point of view,
   formatting habits, humour, how CTAs are phrased.
3. Write the voice guide: a one-line voice summary, three to five traits
   each with "this, not that" pairs, a do/don't list, a word bank, rhythm
   rules and two short before/after rewrites as proof.
4. Quote only short fragments from the samples as evidence for each trait.
5. When applying the guide, rewrite the target text, then list which rules
   changed what. Keep facts identical; voice changes style, never claims.

Template and analysis checklist are in `references/voice.md`.

## Workflow 5: Post review

**Inputs:** the draft, platform, goal, audience, any image or video
description.

**Steps:** score each criterion 1-5 with one line of evidence, then fix.

| Criterion | What to check |
|-----------|---------------|
| Hook strength | Does the first line (or first 2 seconds) earn the next? Specific, not generic? |
| Clarity | One idea? Could a newcomer restate it in a sentence? Jargon defined or removed? |
| Scannability | Short paragraphs, line breaks, lists where it helps, no wall of text |
| CTA | One clear next step that matches the goal; not engagement bait |
| Platform fit | Within limits, native format, link placement suits the platform |
| Accessibility | Alt text present, CamelCase hashtags, no Unicode "fonts", emoji used sparingly and not mid-sentence, captions on video, sufficient contrast noted for text-on-image |
| Honesty | Claims sourced, results real, sponsorship or affiliation disclosed, no fake scarcity |

Then deliver: the scores table, the top three changes in priority order, the
improved version (within limits, in the user's voice), and alt text if any
visual is involved. Do not lengthen a post that is already working; say so.

## Ethics check (run on every output)

These are non-negotiable. If a request needs any of the following, decline that
part, explain briefly, and offer the honest alternative. Details and examples
are in `references/ethics.md`.

1. **No fake engagement.** Do not plan or write content for buying followers,
   likes, comments or views, engagement pods, sockpuppet accounts, or
   coordinated inauthentic replies.
2. **No fake reviews or testimonials.** Never write a review, testimonial or
   "customer story" that did not happen, and never present AI-written text as a
   real customer's words. Real testimonials may be lightly edited only with the
   customer's approval and without changing meaning.
3. **No posing as an unaffiliated customer.** The user (or their staff,
   friends, investors) must not post praise as if they were independent. Write
   founder posts as the founder: "I built this" or "my company".
4. **Disclose material connections.** Sponsorships, paid partnerships, free
   products, affiliate links, ownership and employment must be disclosed
   clearly and up front, not buried in hashtags or after the fold. Use the
   platform's paid-partnership label when it exists, and plain words such as
   "#ad", "Sponsored", "Paid partnership with X", "Affiliate link" or "I built
   this". This follows the US FTC Endorsement Guides and Consumer Reviews and
   Testimonials Rule; other countries have similar rules.
5. **No engagement bait.** Avoid "comment YES if...", "tag 3 friends", "like
   if you agree, share if you don't" and vote-baiting reactions; platforms
   demote it. A genuine question is fine.
6. **No invented statistics or sources.** Every number needs a source the user
   can point to. Do not attribute quotes to real people who did not say them.
7. **No fake urgency or scarcity.** Only state deadlines and stock limits that
   are true.
8. **Sensitive claims.** Health, financial, legal and weight-loss claims need
   evidence and appropriate caveats; do not promise outcomes. Suggest the user
   check regulated-industry rules with a qualified advisor.

When disclosure is required, put it in the post itself (first line or before
the fold for long posts, on screen and spoken for video), not only in a bio.

## Output conventions

- Lead with the deliverable; keep commentary short and after it.
- Show character counts as `(241/280)` next to platform drafts.
- Use `[ADD: ...]` for missing facts and `[CHECK: ...]` for facts to verify.
- Offer one alternative version only when the trade-off is real (for example,
  a thread versus a single long post).

## Edge cases

- **No source, just a topic:** draft from the user's stated expertise only;
  mark any factual claim `[CHECK]` and suggest the user add a personal example.
- **Source is someone else's work:** summarise and credit it, link to it, do
  not reproduce long passages, and frame the post as commentary.
- **User asks for "viral" content:** explain that reach is not guaranteed,
  then optimise the controllable parts: hook, clarity, format, timing,
  replies.
- **Limits changed:** if the user says a platform's limit differs, trust the
  user, note the date, and suggest updating `references/platforms.md`.
- **Non-English audience:** write natively in that language rather than
  translating line by line; re-check character counts.
- **Regulated industries:** add a note recommending compliance review before
  publishing.
