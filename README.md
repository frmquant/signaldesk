# 📡 SignalDesk

**Your scattered market signals → one daily read of what to focus on.**

SignalDesk is an AI daily risk-briefing agent for traders. Instead of checking five
separate tools each morning, you keep one personal signal desk — pick the signals you
track, enter (or auto-fetch) today's readings — and **Muse Spark** synthesizes them into
a single briefing: today's risk temperature, the three things to focus on, what moved,
and what to watch.

Built for the **Meta Global AI Developer Hackathon** · Track: Indie Developer ·
Problem statement: **Build for Your World**.

> ⚠️ **Decision-support only.** SignalDesk summarizes signals and surfaces what to watch.
> It is **not financial advice** and never tells you to buy or sell.

---

## The problem (one I live firsthand)

A trader's morning is scattered across tools: an index tape here, a volatility gauge
there, rates, the dollar, crypto, correlations. The signals exist — the *synthesis*
doesn't. You end up holding ten numbers in your head and still unsure what today is
really about. SignalDesk does the synthesis: it reads the signals and tells you the one
thing that matters — what to focus on today.

## What it does

- **Build your own signal desk** — pick from a catalog (indices, volatility, rates, FX,
  commodities, crypto, breadth) or add your own; your watchlist is remembered on your device.
- **Daily briefing from Muse Spark** — a risk temperature (risk-on / neutral / risk-off)
  with a 0–100 score, a one-line headline, per-signal reads, **3 focus items**, what moved,
  and what to watch.
- **Live data (optional)** — with Muse Spark **web-search grounding** enabled, the agent
  fetches today's readings itself; otherwise it works only from the numbers you enter
  (it never invents figures).
- **Ask follow-ups** — a built-in chat to probe today's read ("what would flip it risk-on?").

## Meta models used

| Model | Role |
| --- | --- |
| **Muse Spark** (Meta Model API) | The reasoning engine — synthesizes signals into the briefing and powers the follow-up chat |
| **Muse Spark web-search grounding** | Optional live-data path — fetches current market readings server-side |

Base URL `https://api.meta.ai/v1`, OpenAI-SDK compatible.

## Run it

1. Open `index.html` (or the hosted GitHub Pages link).
2. Paste your **Meta Model API key** in the top bar. *(The key stays in your browser tab
   only — it is never saved and never committed to this repo.)*
3. Pick your signals, enter today's readings (or turn on live grounding), and hit
   **Generate**.

No build step — it's a single self-contained page.

## Built during the hackathon

This project was built during the Meta Global AI Developer Hackathon (Oct 26 – Nov 4, 2026).

## Tech

Single-file HTML/CSS/JS. No framework, no backend — the browser calls the Meta Model API
directly with a key the user supplies at runtime.

## License

MIT
