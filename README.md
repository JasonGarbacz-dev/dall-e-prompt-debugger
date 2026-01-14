# DALL·E Prompt Debugger (Custom GPT)

**DALL·E Prompt Debugger** is a custom GPT built to turn messy, ambiguous image ideas into *clear, controllable, reproducible* prompts for image generation—while making the “prompting” process transparent and editable. It behaves less like a magic box and more like a visible compiler: it shows how your words get translated into the final prompt that drives the model.

This is designed for anyone who wants dependable outputs (designers, product teams, marketers), and it’s especially useful for recruiters/hiring managers evaluating applied AI engineering instincts: ambiguity handling, structured reasoning, reproducibility, and user-centric tooling.

---

## What it does (in plain English)

### 1) Converts vague ideas into structured intent
When a user describes an image, the GPT first breaks the request into clear components, such as:
- **Subjects** (what’s in the image)
- **Actions** (what’s happening)
- **Setting** (where it takes place)
- **Lighting** (how it’s lit)
- **Style** (photo, illustration, cinematic, etc.)
- **Mood** (playful, tense, dreamy, minimal, etc.)
- **Constraints** (e.g., “no gore,” “no people,” “brand colors,” etc.)

**Benefit:** Users don’t need to know prompt “magic words.” They get a clean mental model of what’s being asked and what’s missing.

---

### 2) Generates an optimized prompt—but doesn’t force it
After interpreting the request, it proposes an **optimized DALL·E prompt** that’s more specific, more consistent, and less error-prone than the raw user text.

Users can then choose:
- **Generate using the optimized prompt**
- **Edit** the optimized prompt (change style, camera angle, time of day, etc.)
- **Use the original text verbatim**
- **Cancel**

**Benefit:** You get better outputs without losing creative control. The user is always in the loop.

---

### 3) Prevents “silent prompt drift”
A major problem in image generation workflows is that systems often rewrite user text in invisible ways. This GPT **never hides** what it’s sending to the image model.

It explicitly shows:
- What the user typed
- What the GPT suggested
- What was actually sent to generation

**Benefit:** Trust and auditability. Teams can review decisions, explain outcomes, and standardize prompt quality.

---

### 4) Produces reproducible prompt traces
After generating an image, it prints a **Prompt Trace Block** containing:
- **User input**
- **Suggested prompt**
- **Final prompt actually used**
- **Model/version**
- **Aspect ratio** (if specified)
- **Timestamp (UTC)**
- Any additional metadata that improves reproducibility

**Benefit:** This supports real workflows—iteration, collaboration, and consistent results across people and time.

---

## Why this matters (value to teams)

### Faster iteration with fewer failed generations
By explicitly controlling details like subject clarity, lighting cues, and camera framing, the GPT reduces the “try 20 times to get close” loop.

### Better alignment between stakeholders
Non-technical collaborators can see the prompt logic and suggest changes (“make it dusk,” “wider shot,” “remove crowd”) without needing to learn prompting.

### Stronger evaluation signal for applied AI engineering
This GPT demonstrates applied engineering behaviors that matter in production AI:
- **Ambiguity resolution** (detecting overloaded terms like “Jaguar” or “model”)
- **Structured decomposition** (turning natural language into controllable parameters)
- **Human-in-the-loop design** (explicit user choice + editability)
- **Reproducibility + traceability** (prompt provenance as a first-class feature)

---

## Example: resolving ambiguity (real-world behavior)
If a user says:  
> “A jaguar chasing a model on a runway with lights.”

The GPT doesn’t assume. It helps disambiguate:
- Jaguar = animal or car?
- Model = person or toy/model car?
- Runway = fashion runway or airport runway?
- Lights = stage lights or headlights?

Then it rewrites the prompt accordingly and allows the user to generate with confidence.

**Benefit:** Fewer wrong generations due to language collisions—one of the most common failure modes in generative UX.

---

## In short
DALL·E Prompt Debugger makes image generation:
- **Clear** (structured intent)
- **Controllable** (editable prompts)
- **Trustworthy** (no hidden rewriting)
- **Repeatable** (prompt traces)

It’s built to feel like a professional tool, not a chatbot—optimized for real iteration cycles and measurable improvements in output quality.

Built by Jason Garbacz

I’m a process optimizer with a builder’s toolkit — I reduce rework with reusable systems.
System instructions available upon request.
