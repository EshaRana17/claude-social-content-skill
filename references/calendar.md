# 30-Day Content Calendar

A calendar is a capacity plan first and a content plan second. Most calendars
fail because they assume more time than the user has.

## Inputs to collect

| Input | Why it matters | Default if missing |
|-------|----------------|--------------------|
| Goal | Decides the CTA mix and metrics | Audience growth |
| Measurable target | Makes the review loop possible | None; suggest one |
| Pillars (3-5) | Keeps topics varied but on-brand | Derive from offer and audience |
| Platforms | Sets formats | The user's one or two most active |
| Weekly capacity | Sets cadence | Ask; do not assume |
| Start date | Dates in CSV | Next Monday |
| Key dates | Launches, events | None |
| Existing long-form | Hero pieces to repurpose | None |

## Pillars

A pillar is a recurring theme the audience values and the user can speak to
credibly. Example set for a solo bookkeeping practice:

| Pillar | Purpose | Weight |
|--------|---------|--------|
| Teach (practical tax and cash-flow tips) | Reach and trust | 40% |
| Behind the work (how I run the practice) | Relatability | 25% |
| Client outcomes (real, with permission) | Proof | 20% |
| Offer (services, booking) | Conversion | 15% |

Tie weights to the goal: growth goals lean on teaching; conversion goals
raise proof and offer, but offer content above about 20-25% usually tires an
audience.

## Cadence by capacity

| Weekly capacity | Suggested cadence |
|-----------------|-------------------|
| 1-2 hours | 1 hero platform, 2-3 posts/week, all repurposed from one weekly idea |
| 3-5 hours | 1-2 platforms, 3-5 posts/week, one long-form or video per week |
| 6-10 hours | 2-3 platforms, near-daily on the primary, 2-3/week on secondary |
| 10+ hours | Multi-platform with a weekly hero piece and daily short-form |

Consistency beats volume. If unsure, pick the lower row and say so.

## Format mix (per platform, monthly)

- **X:** mostly single posts, 2-4 threads, replies counted as real work.
- **LinkedIn:** text posts, 2-4 document/carousel posts, 1-2 personal stories.
- **Instagram:** carousels for teaching, Reels for reach, Stories for
  day-to-day (Stories optional in the calendar).
- **TikTok / Shorts:** 2-5 videos per week if video is a priority; batch film.
- **Threads / Bluesky:** short opinions and conversation; low production.

## The hero-and-repurpose rhythm

1. Week 1 hero: one long-form piece (article, video, podcast episode).
2. Days following: repurpose into 4-8 posts across platforms.
3. Repeat weekly, or every two weeks at low capacity.
4. Recycle best performers from earlier months with a new hook (note that
   it is a repost if the platform audience would notice).

## Building the 30 days

1. Place key dates first.
2. Place hero pieces (1 per week or per fortnight).
3. Fill repurposed posts after each hero.
4. Fill remaining slots by pillar weights.
5. Leave 1 buffer slot per week (status `buffer`) for timely topics or rest.
6. Check variety: no pillar three days in a row, no format five days in a row.
7. Write a working hook for every row, not just a topic.

## CSV format

Use the exact header from `assets/content_calendar.csv`:

```
date,day,platform,pillar,format,working_title_or_hook,cta,asset_needed,repurposed_from,disclosure_needed,status,notes
```

- `date`: YYYY-MM-DD
- `day`: Mon-Sun
- `platform`: X, LinkedIn, Instagram, TikTok, YouTube Shorts, Threads, Bluesky
- `format`: post, thread, carousel, document, reel, short, story, video, live
- `cta`: the single next step
- `asset_needed`: image, slides, video, none
- `repurposed_from`: date or title of the hero piece, or blank
- `disclosure_needed`: no / ad / affiliate / own-product / gifted
- `status`: idea, drafted, scheduled, published, buffer
- Quote any field containing a comma.

Provide both a Markdown table (for reading) and the CSV block (for import).

## Weekly review loop

Choose three metrics that match the goal, then pre-commit to actions:

| Goal | Metrics | If low | If high |
|------|---------|--------|---------|
| Growth | Reach, follows per post, shares | Test new hooks; post when audience is active | Make a follow-up or series |
| Trust | Saves, comments with substance, replies | More specifics and examples | Turn into a lead magnet or longer piece |
| Conversion | Link clicks, sign-ups, DMs about the offer | Clarify the offer; add proof | Increase offer slot slightly |

Review once a week for 20 minutes. Change one variable at a time.
