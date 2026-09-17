# Waste Sort Assistant
An AI-powered household waste classification tool, built as the final project for the **1M1B – IBM SkillsBuild AI for Sustainability Virtual Internship** (in collaboration with AICTE).

**Live demo:** _(add your GitHub Pages link here once enabled — e.g. `https://ratanashish.github.io/waste-sort-assistant/`)_

---

## Problem Statement
How might we use AI to identify and classify household waste, so that segregation at source becomes accurate and easy for everyone?

Households and campuses routinely mix wet, dry, e-waste, and hazardous waste — not out of unwillingness, but because there is no quick, reliable way to know which category an item belongs to at the moment of disposal.

## SDG Alignment
- **Primary:** SDG 12 — Responsible Consumption and Production
- **Secondary:** SDG 11 — Sustainable Cities and Communities

## How It Works
1. **Input** — the user types the name of any waste item
2. **Classification** — the item is matched against one of four categories: *Wet/Biodegradable, Dry/Recyclable, E-Waste, Hazardous*
3. **Guidance** — the tool returns a short disposal instruction and a plain-language reason

This repository contains a standalone, offline-capable build (`index.html`) that uses a transparent, keyword-based rule engine so the demo works on any static host, including GitHub Pages, without needing an API key or network access.

In the production design, the same input/output contract (category, instruction, reason as structured JSON) is intended to be served by a prompt-engineered large language model call, which generalises to items outside any fixed keyword list. The system prompt used for that design is documented in the comments inside `index.html`.

## Target Users
- Households segregating waste daily
- Campus students at hostel/canteen waste points
- Municipal workers needing fast sorting guidance on-site

## Responsible AI Considerations
- **Fairness:** category rules cover common urban and rural waste items, avoiding bias toward any one region's habits
- **Transparency:** every classification includes a plain-language reason, not a black-box answer
- **Ethics:** the tool only advises on disposal; it is never used for surveillance or profiling of users
- **Privacy:** no personal or location data is collected or stored — only the item name is processed, and nothing is saved

## Expected Impact
Better segregation at source → higher recycling accuracy, lower landfill burden, and reduced downstream sorting cost for municipal bodies.

## Tech Stack
Plain HTML, CSS, and JavaScript — no framework, no build step, no external dependencies. Runs entirely client-side.

## Running Locally
Just open `index.html` in any browser — no installation needed.
