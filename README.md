# Ajaib Community Feed Prototype

Interactive prototype of a social investing feed, recreated pixel-faithfully from Figma and extended with a full interaction model. Built as a single self-contained HTML file — no build step, no dependencies beyond Google Fonts.

**Live demo:** https://randyvarianda.github.io/ajaib-feed-prototype/

## Screens

1. **Feed (Insight – Trending)** — 19 posts across three market segments, trending filter pills, post composer entry, FAB
2. **Post detail / thread** — original post, comment thread with nested replies, expandable hidden replies, reply composer
3. **Buat Postingan** — compose flow with audience selector, live character counter, and Posting enable states
4. **Profil** — dynamic per-user profile: identity, Spesialis badge, stats, bio, follow, and the user's actual posts

## Trust badge system (Spesialis)

The core concept under evaluation: **scoped, evidence-adjacent trust badges** instead of generic achievement badges.

- Three scopes: `Spesialis Saham ID` 🇮🇩, `Spesialis Saham US` 🇺🇸, `Spesialis Crypto` ₿
- One visual system: tinted label (4px radius, 2×4px padding) with leading SVG flag/coin icon
- **Contextual display rule:** the badge only renders on posts matching its scope. RatuBanteng's ID badge shows on her $BBCA post and is absent on her $BTC post; ShirohigePirate's Crypto badge shows on his $BTC post and never on his $BBCA comments
- Tap any badge → popup with criteria, earned date, and compliance copy (incl. the "bukan rekomendasi investasi" disclaimer for licensed scopes)

## Timestamp system

Relative-decay format, per spec: `baru saja` → `45m` → `5j` (jam) → `2h` (hari) → `12 Jun` (this year) → `1 Sep 2023` (older). All stages are visible in the feed. Absolute timestamps remain on transaction records (stock widget).

## Interactions

- Like toggle with pop/burst animation (posts + comments), follow/Diikuti toggles
- Comment → thread navigation; per-post threads with comment counters and empty states
- Reply with auto `@mention`, reply-context chip with cancel, one-level nesting with indent
- "Lihat semua balasan" expand/collapse
- Posting adds a real post to the feed; commenting appends to the thread and bumps counters
- Tap any username/avatar → their profile, assembled from live feed data

## Tech notes

- All icons are inline Phosphor SVG; avatars are inline SVG initials; badges are inline SVG — zero external image dependencies
- Design tokens as CSS variables, extracted from the Figma source (Lato type scale, Ajaib UI Light palette)
- Best viewed at 360–480px width; runs offline

## Content disclaimer

All usernames, posts, statistics, and badge criteria are fictional placeholder content for design evaluation. Nothing here is investment advice.
