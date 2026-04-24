# Daily Dev Quote – Personal Inspiration

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python 3.x](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)](https://www.python.org/)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-YAML-2088FF?logo=github-actions&logoColor=white)](.github/workflows/daily-quote.yml)
[![API](https://img.shields.io/badge/API-DummyJSON-ff69b4)](https://dummyjson.com/quotes/random)

> "I Paint Self-Portraits Because I Am So Often Alone, Because I Am The Person I Know Best." — Frida Kahlo

---

This repository does one simple thing: **every day at 08:00 UTC, a GitHub Action fetches a random programming quote and commits it to the README.**

The result is a constantly evolving `README.md` that greets visitors with a new, hand-picked (by an API) quote each day.

---

## Why does this repo exist?

I built this for one reason:

**A personal dose of daily inspiration** – I genuinely enjoy reading a short, thoughtful quote about coding, creativity, or persistence every morning.

The real goal is to:

- Practice writing clean, scheduled workflows
- Experiment with public APIs and JSON parsing
- Keep a live "digital sticky note" of wisdom on my profile

---

## How it works

- A **GitHub Action** (`.github/workflows/daily-quote.yml`) runs every day via a `cron` schedule.
- The action checks out the repo, sets up Python, and runs `update_quote.py`.
- The Python script:
  - Calls the free [DummyJSON Quotes API](https://dummyjson.com/quotes/random) (no API key needed)
  - Extracts a random quote and author
  - Overwrites `README.md` with a fresh template containing the new quote and a timestamp
- If the quote has changed (which it always will), the action commits and pushes the update.

---

## Tech stack

| Component       | Technology                                      |
|----------------|-------------------------------------------------|
| Automation      | GitHub Actions (scheduled + manual triggers)   |
| Scripting       | Python 3 + `requests` library                  |
| API             | [dummyjson.com/quotes/random](https://dummyjson.com/quotes/random) |
| Version control | Git / GitHub                                   |

---

## Running it yourself

You can fork this repo and adapt it to your own taste – change the API endpoint, update the quote template, or switch to a different schedule.

To test it manually:

1. Go to the **Actions** tab of your fork
2. Select the **Daily Quote Update** workflow
3. Click **Run workflow** → **Run workflow**

Within a minute you'll see a new commit on your main branch.

---

## License

MIT – do whatever you want with the code. Go build your own automated quote machine, or turn it into a daily dad-joke bot.
