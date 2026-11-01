# Platform Reference

Limits change. Each row records the value, the date it was last checked, and
how confident the check was. When the user reports a different number, trust
the user and update this file.

**Last full review: 2026-11-01.** Checked against platform help pages where
available and cross-checked with several independent scheduling-tool
references. "Confirmed" means multiple consistent sources; "Conflicting" means
sources disagreed and the safer (lower) number is used for drafting.

## Hard limits

| Platform | Item | Limit | Checked | Status / note |
|----------|------|-------|---------|---------------|
| X | Post (free account) | 280 weighted characters | 2026-11-01 | Confirmed. URLs count as 23 characters regardless of length. Some characters (CJK, many emoji) count as 2. |
| X | Post (Premium) | 25,000 characters | 2026-11-01 | Confirmed. Only the first ~280 show before "Show more"; draft as if 280 matters. |
| X | Images per post | 4 | 2026-11-01 | Long-standing; confirm if mixing media. |
| LinkedIn | Personal or page post | 3,000 characters | 2026-11-01 | Confirmed. Text truncates behind "...see more" after roughly the first 2-3 lines (about 200 characters on mobile; varies by device). |
| LinkedIn | Document (PDF) post | Many pages; keep 6-12 | 2026-11-01 | Use for carousel-style decks. Add a title; alt text is limited for documents, so describe key visuals in the post text. |
| Instagram | Caption | 2,200 characters | 2026-11-01 | Confirmed. Truncates after about 125 characters in feed. |
| Instagram | Hashtags per post | 5 | 2026-11-01 | Conflicting. Instagram announced a 5-hashtag cap in December 2025; some pages still cite 30. Draft with 5 or fewer. |
| Instagram | Carousel items | 20 photos/videos | 2026-11-01 | Confirmed across sources (raised from 10 in August 2024). Some schedulers still cap at 10 via API. |
| Instagram | Alt text | Supported per image (Advanced settings) | 2026-11-01 | Always provide. |
| Threads | Post | 500 characters | 2026-11-01 | Confirmed. Links reported not to count against the limit. |
| Bluesky | Post | 300 graphemes | 2026-11-01 | Confirmed. Unit is graphemes (user-perceived characters); links count at full length unless shortened by the client. Up to 4 images. |
| TikTok | Caption | 2,200 safe (4,000 in-app) | 2026-11-01 | Conflicting. 4,000 reported for captions typed in the app; 2,200 reported via posting APIs and schedulers. Draft to 2,200. |
| YouTube Shorts | Length | Up to 3 minutes | 2026-11-01 | Conflicting. YouTube raised Shorts to 3 minutes in October 2024; some sources still say 60 seconds. Script hook-first regardless. |
| Instagram Reels | Length | Varies by account and entry point | 2026-11-01 | Not verified. Script 15-90 seconds unless the user says otherwise. |

If a draft is within 5% of a limit, shorten it. Counting differs between
tools (characters, graphemes, UTF-16 units), so the margin protects the user.

## Platform norms (judgement, not rules)

### X
- First post must stand alone; most readers never open the thread.
- One idea per post in a thread. Number posts (1/, 2/) only if the voice does.
- External links tend to get less distribution than native content; put the
  link in the last post or the first reply and say where it is.
- Short, declarative sentences. Line breaks help scanning.
- 0-2 hashtags; often none.

### LinkedIn
- The first two lines are the hook; everything else is behind the fold.
- Short paragraphs (1-3 lines), white space, a single takeaway.
- First-person experience and specific lessons beat generic advice.
- Up to 3 relevant hashtags at the end, CamelCase.
- Native documents (PDF carousels) work well for step-by-step material.
- Avoid "Agree?" as a whole CTA; ask a real question.

### Instagram (feed and carousels)
- Carousel cover slide: a clear promise in 6-10 words, large type.
- One idea per slide, 15-40 words of body text maximum.
- Second slide should reward the swipe immediately.
- Last slide: summary or CTA (save, share with someone it helps, visit link in
  bio). Links in captions are not clickable.
- Caption opens with a hook before the ~125-character truncation, expands on
  the carousel, ends with CTA, then hashtags.
- Recommended aspect ratio for feed: 4:5 portrait (1080x1350) is a common
  safe choice; keep all slides the same ratio.

### Short video (TikTok, Reels, Shorts)
- Hook in the first 1-3 seconds, both spoken and as on-screen text.
- A visual change every 2-4 seconds (cut, angle, B-roll, text pop).
- Burned-in or auto captions always; many viewers watch muted.
- Keep on-screen text inside safe zones (avoid bottom ~20% and right edge
  where buttons sit).
- Vertical 9:16, 1080x1920.
- One CTA, near the end, or a loopable ending.

### Threads
- Conversational, lower polish, replies matter.
- Text-first; images optional.
- Topic tag (one per post) instead of hashtag stacks.

### Bluesky
- Short, direct, community-minded; self-promotion lands better with context.
- Alt text culture is strong: always include it.
- Use the client's link card for links instead of raw URLs where possible.
- Feeds are user-chosen; hashtags help custom feeds pick posts up.

## Disclosure tools by platform

| Platform | Built-in tool | Plus |
|----------|---------------|------|
| Instagram, Facebook | "Paid partnership" label | Still say it in the caption for clarity |
| TikTok | Content disclosure / "Paid partnership" toggle | Spoken or on-screen disclosure |
| YouTube | "Includes paid promotion" checkbox | Verbal disclosure in the video |
| X, LinkedIn, Threads, Bluesky | No universal label for organic posts | "#ad", "Sponsored", "Paid partnership with ..." at the start |

Labels and toggle names change; if unsure, tell the user to check the
platform's current branded-content policy.

## Re-verification checklist

When updating this file:
1. Check the platform's own help center first.
2. Cross-check with at least two independent sources.
3. Record the date and mark Confirmed or Conflicting.
4. If conflicting, draft to the lower number.
