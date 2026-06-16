# 🎌 Nami — Your Anime Bestie

> *An AI-powered anime recommendation agent that feels like texting your most knowledgeable anime friend.*

**Live demo:** [niv-ships.github.io/Nami](https://niv-ships.github.io/Nami/)

-----

## The Problem

Anime recommendation is a solved problem — or so it seems. MAL, AniList, Kitsu, and a dozen AI chatbots all claim to recommend anime. But after looking at the landscape, I noticed something:

- Existing tools are **history-based** — they need your watch history, ratings, and an account before they’ll help you
- AI chatbots in this space are almost entirely **roleplay/companion bots**, not recommendation tools
- Nobody was doing **mood-based, conversational recommendations** — the kind where you just describe how you’re feeling right now and get a personalised answer instantly

That’s the gap Nami fills.

-----

## The North Star

> *“It should feel like texting a new friend you just found out loves anime as much as you.”*

This one sentence drove every product decision:

- No forms. No dropdowns. No “rate these 10 shows first.”
- Max 2 questions before recommending — hold the user’s attention
- Warm, casual language — friend energy, not algorithm energy
- Recommendations with *personal reasons*, not just titles

-----

## What Nami Does

1. **Greets you first** — no cold empty chat box
1. **Asks 1-2 natural questions** about your mood and preferences
1. **Recommends 2-3 anime** with an enthusiastic personal reason for each
1. **Shows real data** — pulls cover art, score, episode count and genres from MyAnimeList via the Jikan API
1. **Links to MAL** for each recommendation so you can explore further
1. **Keeps going** — ask for more, pivot the vibe, she adapts

-----

## How It’s Built

|Layer            |Technology                                   |
|-----------------|---------------------------------------------|
|Conversational AI|Claude API (claude-sonnet-4-6)               |
|Anime Data       |Jikan API (unofficial MAL API, free, no auth)|
|Frontend         |Vanilla HTML/CSS/JS                          |
|Hosting          |GitHub Pages                                 |

**The key insight:** Nami’s personality lives entirely in the system prompt — a carefully crafted brief that tells Claude how to behave, what tone to use, what rules to follow, and crucially, how to format recommendations so the app can detect anime titles and fetch real data automatically.

Changing one line of the system prompt changes the entire user experience. This is prompt engineering as product design.

-----

## What I Learned

- **The gap is in UX, not data.** The anime recommendation space has plenty of data. What it lacks is a human, frictionless experience.
- **Examples beat instructions.** Telling Claude “use this format” didn’t work. Showing Claude exactly what correct output looks like did. A lesson that applies to managing people too.
- **Shipping beats perfecting.** Nami launched with no database, no login, no memory. She works anyway — because the core user need (find something to watch right now) is met.

-----

## What’s Next

- [ ] JustWatch integration — show exactly where to stream in your country
- [ ] Session memory — Nami remembers what you’ve watched across conversations
- [ ] “I’ve seen this” button — build a watched list on the fly
- [ ] Rich cards with trailers

-----

## About

Built by [@niv-ships](https://github.com/niv-ships) — a PM with 8 years of experience who believes the best way to understand a product is to build it.

*Still sailing. 🏴‍☠️*
