# Insight Feed Prototype

Interactive 3-screen prototype of a fintech community feed, recreated pixel-faithfully from Figma.

**Live demo:** https://randyvarianda.github.io/insight-feed-prototype/

## Screens
1. **Feed (Insight - Trending)** — trending pills, post cards, stock widget, liked-by stacks
2. **Comment detail (Creator Reply)** — threaded comments, author replies, reply composer
3. **Buat Postingan** — compose flow with live character counter

## Interactions
- Like toggle with pop animation (posts + comments)
- Follow / Diikuti toggle
- Comment icon → detail screen, back navigation
- FAB / composer field → compose screen; posting adds your post to the feed
- Live reply + compose inputs with enable states

## Tech
Single self-contained HTML file — inline Phosphor icons, SVG placeholder avatars, design tokens as CSS variables. Only external dependency is Google Fonts (Lato). Best viewed at 360px width.
