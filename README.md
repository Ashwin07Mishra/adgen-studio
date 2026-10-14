<div align="center">

# AdGEN Studio

### From brand brief to a checked, shootable AI ad — in one page.

**Brand + script + product shots &rarr; storyboard sheet &rarr; Seedance video &rarr; final cut.**
Every step rated, gated and verified before a single credit is spent.

`LLM scriptwriting` · `GPT Image 2 storyboards` · `Seedance 2.0 video` · `Vision QA` · `Hard-gated spend`

</div>

---

## The problem

Making one AI-generated ad today means juggling an LLM, an image model and a video model by hand: copy a script here, paste a prompt there, re-upload product photos, and hope the headphones still look like the headphones. Logos get garbled. A second product sneaks into the shot. The model casts a different person in every frame. And each retry costs real money.

## The answer

**AdGEN Studio replaces the manual copy/paste flow between an LLM, GPT Image 2 and Seedance.** You describe the brand once, write a short brief, and the studio walks you through five gated steps — scoring and checking the work at every stage, and refusing to spend until you explicitly confirm.

---

## The five-step flow

| # | Step | What happens |
|---|------|--------------|
| 1 | **Brand & product shots** | A reusable brand profile: product lock, exact product name, approved colours, casting, avoid-words and standing rules. Upload your pack shots and pick the angles to use. |
| 2 | **Prompt → features → script** | Write the one thing only you can: the brief. The studio extracts the features to highlight and writes a timed, voice-over-ready script — rated out of 100. |
| 3 | **Storyboard** | An engineered storyboard prompt, then a multi-panel storyboard sheet generated *from your real product photos*, followed by a vision check against those photos. |
| 4 | **Video** | Pick a Seedance 2.0 tier and resolution. A production direction is auto-built from the script, product lock and voice note, checked, and gated behind a human approval list. |
| 5 | **Final cut** | The generated ad lands in the page. Add real, crisp on-screen supers (rendered as true text, never AI-garbled), then run a final vision check against the photos and script. |

---

## What makes it different

### Rated, explained, fixable
Every script and prompt gets a **rating out of 100** with a full breakdown: *Fix these* and *Working*, each check named and explained. Edit by hand and **Re-check**, or hit **AI enhance** to rewrite once from the specific fixes. Nothing is ever rewritten behind your back.

### Hard gates, not suggestions
Rules are enforced by code, not left to the model's goodwill. The server **blocks paid storyboard and video calls** when a hard rule fails, unless you consciously override it. Checks include:

- exact product name — any other spelling is blocked
- approved colour palette — anything else is blocked
- avoid-list words, checked in every script and prompt
- product lock embedded in every prompt
- casting description present, so the **same person** appears in every frame
- "exactly one pair" and no-glitch clauses, to stop duplicated products and face/hand artefacts
- sufficient product angles sent as references
- no stray on-screen text or logos

### Vision QA on the output
After generation, a vision model inspects the **storyboard against your product photos** (panel by panel: product fidelity, garbled text, invented parts, duplicated items, casting consistency) and the **video against your photos and script** (including whether the voice-over matches). Results are advisory — you stay in charge — but defects are caught *before* you move on.

### Human approval before the expensive step
A five-point approval list must be ticked before video generation: product colour/shape/details, no wrong or added text, no invented controls, same person and wardrobe throughout, every script beat present and in order.

### Two-click spend confirmation
Paid actions **arm first**: the button turns red and reads *"SPENDS CREDITS … click again to confirm"*, then disarms on its own. Accidental spend is designed out of the interface, and the server independently requires an explicit confirmation too.

### Casting that stays consistent
A casting reference photo is passed alongside product shots so the talent keeps the same face, skin tone and wardrobe across the whole film.

### Real supers, not AI typography
On-screen text is added in post with ffmpeg as genuine text. No garbled lettering, no gibberish end cards.

### Resumable by design
Long renders are tracked as pending tasks. Close the tab, come back, reopen the ad — it resumes where it was, and results are downloaded the moment they complete.

---

## Built for brands, not demos

- **Per-brand profiles** hold the standing rules once, so nobody retypes "don't alter the product" ever again.
- **Past ads** are saved as runs you can reopen, inspect and iterate.
- **Describe from photos** drafts the product-lock description straight from your pack shots, ready for you to correct.
- **Language and voice notes** per brand for voice-over direction.
- **Brand-safe by default:** no competitor marks, no invented claims, live-action-only unless you opt into named effects.

---

## Under the hood

- **Prompt engineering:** an LLM writes the script and storyboard prompt against a per-brand schema, then every output is scored by deterministic code checks plus model-judged checks.
- **Image:** GPT Image 2 (edit mode) with product shots and a casting portrait as reference images; selectable quality and resolution.
- **Video:** Seedance 2.0 Mini / Fast / Pro, 480p–1080p, 4–15 s, with the approved storyboard and product shots as references and optional music/sound controls.
- **Vision QA:** a multimodal model reviews storyboards and videos against ground-truth photos.
- **Finishing:** ffmpeg for supers and assembly.
- **Interface:** a single-page, no-framework local web app with a stepper, colour-coded rating pills and locked-until-ready sections.

---

## Proven on a real product

The studio was exercised end-to-end on a premium headphone launch: a 15-second airport-to-studio film with a consistent on-screen talent, a legible product wordmark, a single correctly-rendered product in every shot, and a scripted voice-over delivered exactly as written. The process surfaced — and the gates now prevent — the classic failure modes of AI ad generation: garbled logos, wrong casting, duplicated products and face glitches.

---

## See it in action

A 64-second product tour, captured live from the working interface, walks through every step above: brand lock, the rated script, the storyboard and its vision check, the video gates and the final cut.

---

## Status

Actively developed. The pipeline is working end-to-end today; next up are longer multi-clip ads (30 s+) assembled from several Seedance clips, team login with server-side keys and spend caps, and a hosted version.

---

## About this repository

This repository is the public overview of AdGEN Studio. The source code is kept private. For a demo, collaboration or early access, open an issue or get in touch.

<div align="center">

**AdGEN Studio** — *write the brief. We'll make sure the ad is right before it costs you anything.*

</div>
