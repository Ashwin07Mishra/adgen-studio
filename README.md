<div align="center">

# 🎬 AdGEN Studio

**From brand brief to a checked, shootable AI ad — in one page.**

![LLM](https://img.shields.io/badge/LLM-Scriptwriting-green)
![Image](https://img.shields.io/badge/Storyboard-GPT%20Image%202-orange)
![Video](https://img.shields.io/badge/Video-Seedance%202.0-blueviolet)
![Vision](https://img.shields.io/badge/Vision-QA%20Enabled-red)
![Gates](https://img.shields.io/badge/Paid%20API-Hard--Gated-critical)
![Frontend](https://img.shields.io/badge/Frontend-Single%20Page%20App-1f4fd8)
![Status](https://img.shields.io/badge/Status-Working%20End--to--End-success)

`🧠 Script` → `🖼️ Storyboard` → `🎥 Video` → `✂️ Final Cut` — every step rated, gated and verified **before** a single paid API call is made.

</div>

---

## 📖 Overview

AdGEN Studio is an AI ad-production platform that turns a **brand profile, a short brief and your real product photos** into a finished video ad. It replaces the manual copy/paste flow between an LLM, GPT Image 2 and Seedance with one guided, five-step interface.

Beyond generation, AdGEN Studio **audits its own work**: scripts and prompts are scored out of 100, code-enforced rules block bad inputs, a vision model checks every storyboard and video against your product photos, and nothing paid runs without an explicit human confirmation.

---

## ⚠️ Problem Statement

Making one AI ad today means juggling three models by hand: copy a script here, paste a prompt there, re-upload photos, and hope the product still looks like the product.

| 💥 What goes wrong | 🔁 What it triggers |
|---|---|
| Logos and product wordmarks come out garbled | A full re-render (more tokens, more paid API calls) |
| A second product sneaks into the shot | A full re-render (more tokens, more paid API calls) |
| The "talent" is a different person in every frame | A full re-render (more tokens, more paid API calls) |
| Wrong colours, invented buttons, gibberish end cards | A full re-render (more tokens, more paid API calls) |
| Someone clicks Generate one time too many | Wasted paid API usage |

AdGEN Studio catches these failures **before** generation and **right after** it, instead of after the token bill.

---

## ✨ Key Features

### 🏷️ Brand Profiles
- Reusable per-brand setup: **product lock**, exact product name, approved colours, casting, avoid-words and standing rules
- Upload pack shots and choose the angles to use
- ✨ *Describe from photos* drafts the product-lock description straight from your images
- Language and voice-over notes per brand
- Past ads saved as runs you can reopen and iterate

### 📝 Rated Script Writing
- Write only the brief; the studio extracts the **features to highlight** and writes a timed, voice-over-ready script
- **Rating out of 100** with a full *Fix these / Working* breakdown
- ✏️ Edit by hand and **Re-check**, or 🪄 **AI enhance** to rewrite once from the specific fixes
- Nothing is ever rewritten behind your back

### 🖼️ Photo-Faithful Storyboards
- Engineered storyboard prompt with its own rating
- Multi-panel sheet generated **from your real product photos** plus a casting portrait
- Selectable quality and resolution

### 🎥 Gated Video Generation
- Seedance 2.0 **Mini / Fast / Pro**, 480p–1080p, 4–15 s
- Production direction auto-built from the script, product lock and voice note, then checked
- ✅ Five-point human approval list before the expensive step

### 🔍 Vision QA
- Storyboard checked **panel by panel** against your photos
- Video checked against photos **and script**, including whether the voice-over matches
- Advisory by design: you stay in charge

### ✂️ Real Supers, Not AI Typography
- On-screen text added in post as genuine text — no garbled lettering, no gibberish end cards

---

## 🛡️ Hard Gates (enforced by code)

| Gate | What it blocks |
|---|---|
| 🏷️ Exact product name | Any other spelling |
| 🎨 Approved colours | Anything off-palette |
| 🚫 Avoid-list | Banned words in any script or prompt |
| 🔒 Product lock | Prompts missing the product description |
| 👤 Casting | Prompts that don't pin the same person in every frame |
| 1️⃣ One-pair / no-glitch clauses | Duplicated products, face and hand artefacts |
| 📸 Reference angles | Too few product angles sent to the model |
| 🔤 No stray text | Invented logos and on-screen text |
| 💳 Paid API confirm | Accidental paid generation (see below) |

> The server **refuses paid storyboard and video calls** when a hard rule fails — unless you consciously override.

### 💳 Two-Click Paid API Confirmation

```text
[ 💳 Generate video ]  ──click──▶  [ ⚠ PAID API CALL: 15 s video, Seedance 2.0 Pro 720p — click again to confirm (8 s) ]
                                              │
                                  second click within 8 s ──▶ generation starts
                                  otherwise ──▶ disarms automatically
```

---

## 🏗️ System Architecture

```text
 🏷️  Brand Profile + Product Shots
            │
            ▼
 📝  Brief  ──▶  🧠 LLM: Features + Script
                          │
                          ▼
              📊 Rating + Code Checks  ◀── fix & re-check
                          │ pass
                          ▼
              🖼️  Storyboard Prompt (rated)
                          │
                          ▼
              🚦 Hard Gates ──── blocked ──▶ back to prompt
                          │ clear
                          ▼
              💳 Paid API call, two-click confirm
                          │
                          ▼
              🖼️  GPT Image 2 Storyboard Sheet
                          │
                          ▼
              🔍 Vision Check vs Product Photos
                          │
                          ▼
              ✅ Human Approval List (5 points)
                          │
                          ▼
              💳 Paid API call, two-click confirm
                          │
                          ▼
              🎥 Seedance 2.0 Video
                          │
                          ▼
              ✂️  Real Supers (ffmpeg)
                          │
                          ▼
              🔍 Video Check vs Photos + Script
                          │
                          ▼
                     🎬 Final Ad
```

---

## 🔄 Workflow

### Step 1 — 🏷️ Brand & Product Shots
Set the brand once: product lock, exact name, colours, casting, avoid-words, standing rules. Upload pack shots and select the angles to use.

### Step 2 — 📝 Prompt → Features → Script
Write the brief. The studio extracts the features, writes the script, and rates it. Fix, re-check or enhance until it's right.

### Step 3 — 🖼️ Storyboard
A storyboard prompt is written and rated, then a multi-panel sheet is generated from your real photos and checked against them.

### Step 4 — 🎥 Video
Choose a Seedance tier and resolution. The direction is auto-built and checked. Tick the five-point approval list, then confirm the paid API call.

### Step 5 — ✂️ Final Cut
The ad lands in the page. Add supers, then run the final vision check against photos and script.

---

## 📊 Sample Rating Report

```text
Rating 90/100      18 of 20 checks passed
Features highlighted:  Advanced noise cancelling · Effortless portability · All-day comfort

✗ Fix these
   claims grounded   — a claim is not in your brief
   hook              — opener is generic; use a striking question or problem

✓ Working
   timeline · row length · VO pace · sign-off · supers · avoid list ·
   product visible · no invented claims · voice natural · every feature shown
```

```text
Vision check 100/100   8 of 8 passed (advisory — you still decide)
   ✓ panel 1–6   product matches the photos, no garbled text, one pair only
   ✓ same person across panels
   ✓ casting matches the brief
```

---

## ✅ Human Approval Before Video

- [ ] Product colour, shape and details match the photos in every panel
- [ ] No wrong, garbled or added text or logos anywhere
- [ ] No invented buttons, controls or parts
- [ ] Same person and wardrobe in every panel
- [ ] Every script beat is there, in order

---

## 🧰 Tech Overview

| Layer | Technology |
|---|---|
| 🧠 Scripting & prompts | Large language model with per-brand rules and scored checks |
| 🖼️ Storyboards | GPT Image 2 (edit mode, reference images) |
| 🎥 Video | Seedance 2.0 Mini / Fast / Pro |
| 🔍 Vision QA | Multimodal model reviewing outputs against ground-truth photos |
| ✂️ Finishing | ffmpeg for supers and assembly |
| 🖥️ Interface | Single-page web app with stepper, rating pills and locked-until-ready sections |

---

## 🏆 Proven on a Real Product

The studio was run end-to-end on a premium headphone launch: a **15-second airport-to-studio film** with consistent on-screen talent, a legible product wordmark, a single correctly-rendered product in every shot and a voice-over delivered exactly as scripted. The process surfaced — and the gates now prevent — the classic failure modes: garbled logos, wrong casting, duplicated products and face glitches.

---

## 🎞️ See It in Action

A **64-second tour captured live from the working interface** walks through every step: brand lock, the rated script, the storyboard and its vision check, the video gates and the final cut.

---

## 🗺️ Roadmap

- [x] Brand profiles with product lock and casting
- [x] Rated scripts and storyboard prompts
- [x] Hard gates and two-click paid API confirmation
- [x] Vision QA on storyboards and videos
- [x] Real supers and final cut
- [x] Resumable long renders
- [ ] Multi-clip ads (30 s+) assembled from several clips
- [ ] Team login with server-side keys and token-usage caps
- [ ] Hosted version

---

## 📬 About This Repository

This is the public overview of AdGEN Studio. The source code is kept private. For a demo, collaboration or early access, open an issue or get in touch.

<div align="center">

**AdGEN Studio** — *write the brief; we make sure the ad is right before a single token is wasted.*

</div>
