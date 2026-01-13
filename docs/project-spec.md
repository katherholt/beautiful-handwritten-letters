# Beautiful Handwritten Letters (WIP)

## Overview

Beautiful Handwritten Letters is an experiment inspired by the fictional BeautifulHandwrittenLetters.com from *Her* (2013).

In the film, letters are intimate and well-written, but the process behind them is opaque and slightly uncanny. This project reframes the act of outsourcing sentiment as a transparent system where AI supports higher-quality creative expression without replacing human authorship.

The output is a short, physical letter printed on a thermal printer.

---

## What this project explores

- Whether voice input helps people express sentiment more naturally than typing
- What happens when AI-generated content becomes a physical artifact
- How much structure is required to reliably generate personal-feeling output

---

## How it works

1. **User provides voice input**
   - IRL: phone + mini microphone  
   - Web: browser microphone input  

2. **System captures short voice input**
   - Prompt focuses on a single person and a single feeling  
   - No freeform storytelling  

3. **AI generates a short letter**
   - Constrained length  
   - Warm, restrained tone  
   - Paired with a small generative Valentine’s-style doodle  

4. **Output is printed**
   - Thermal printer produces a single physical copy  
   - The printed artifact is the final product  

---

## Tech setup

### Hardware

- Thermal printer  
- Raspberry Pi (local controller)  
- Smartphone (used as microphone for physical setup)  

### Software

- Speech-to-text API  
- Text generation model  
- Lightweight server running on Raspberry Pi  
- Printer driver for formatted text + graphics  

### Web version

- Hosted on project domain  
- Browser-based microphone input  
- Same generation pipeline  
- Digital preview instead of print  

---

## Constraints

- No editing before printing  
- Single-shot generation  
- Short-form only  
- Output must feel intentional and high quality each time  

These constraints are deliberate and designed to reward clarity of input over iterative refinement.

---

## Input instructions

**Instruction to user (spoken or written):**

1. **Anchor the person**  
   Tell me who this letter is for and the relationship in one sentence.  
   Include how long you’ve known them and where you are right now (physically or emotionally).

2. **Surface the emotional tension**  
   Say one thing you’re holding right now about them — something you miss, regret, forgive, or feel tender about.  
   It doesn’t have to be resolved.

3. **Capture a small, specific detail**  
   Describe one small, ordinary thing about them that you love — a habit, flaw, gesture, or moment that only you would notice.

---

## Generation prompt

Generate a short, sentimental letter with gentle warmth.

**Constraints:**
- 2–3 sentences total  
- Simple, plain language  
- Sentimental and appreciative, not romantic or longing  
- Calm, steady tone (no ache, yearning, or drama)  
- Appropriate for close non-romantic relationships by default  
- No clichés, no abstraction, no metaphor-heavy language  
- No imitation of existing works  
- Avoid intensity unless explicitly prompted  

**Structure:**
- Optional direct address (e.g. “Dear Mom,”)  
- Reference one shared symbol, habit, or small detail  
- Emphasize appreciation, presence, or support  
- End with gratitude or quiet affection  

**Formatting:**
- Hard wrap to `{{LINE_WIDTH}}` characters per line  
- Include a simple Unicode heart border at top and bottom  
- Output must be printer-safe (monospace-friendly)  

**Inputs:**
- Context: `{{ANCHOR}}`  
- Feeling: `{{TENSION}}` (interpreted as appreciation unless stated otherwise)  
- Detail: `{{DETAIL}}`  

**Default mode:** sentimental, grounded, non-romantic.

---

## Example output

♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡

Dear Mom,

Whenever I see angel
numbers, I think of you,
because you always notice
them first and point them
out.

They remind me of how
supported and cared for
I’ve felt lately, and how
easy it’s been to talk and
ask for your advice.

I’m really grateful for
you and for the way you
show up for me.

♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡ ♡


---

## Next steps

- Order and test thermal printer  
- Order Raspberry Pi  
- Locate and test mini microphone  
- Add system sketch to document  
- Outline failure modes and success criteria
