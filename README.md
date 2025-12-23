# CalmSync

**A Reasoning-Driven Meditation Assistant Powered by Gemini 3**

## Overview

CalmSync is a web-based meditation assistant that uses Gemini 3 Pro to autonomously reason over a user's Google Calendar and generate context-aware guided meditations at optimal moments throughout the day. Unlike traditional meditation apps that rely on static scripts or user selection, CalmSync positions Gemini as an intelligent decision-maker. The model determines when an intervention is needed, what type of meditation is appropriate, and how it should be delivered based on cognitive load inferred from calendar events.

The result is a personalized, adaptive experience that feels anticipatory rather than reactive.

---

## Target Users

- Students with dense schedules
- Professionals with frequent context switching
- Anyone seeking lightweight, practical mindfulness integrated into daily routines

---

## Core User Flow

### Step 1: Calendar Ingestion
The user connects Google Calendar (read-only access). CalmSync retrieves:
- Event titles
- Durations
- Gaps between events
- Keywords indicating cognitive or emotional demand (e.g., "interview," "deadline," "presentation", "evaluation", "test", "assessment")

### Step 2: Reasoning & Cognitive Load Analysis (Gemini 3 Pro)
Gemini 3 Pro analyzes the upcoming day and reasons about:
- Event density and transitions
- Likely mental fatigue points
- High-stakes vs low-stakes moments
- Opportunities for short, effective interventions

This reasoning step produces a **Meditation Strategy Plan**, including:
- Whether a meditation is beneficial
- Optimal timing (before, between, or after events)
- Recommended duration
- Style (grounding, energizing, decompression)
- Guidance intensity (silent, lightly guided, fully guided)

**This reasoning layer is the core intellectual contribution of the project.**

### Step 3: Context-Aware Script Generation (Text)
Gemini generates a situational meditation script that explicitly references the user's context, for example:
- Transitions between demanding events
- End-of-day cognitive decompression
- Pre-performance grounding

Scripts are short (30–180 seconds) and avoid generic mindfulness phrasing.

### Step 4: Audio Generation
The generated script is converted into audio using Gemini's speech synthesis capabilities, with:
- Pacing matched to available time
- Intentional pauses
- Tone selected based on meditation style

Audio is delivered directly in the web app.

### Step 5: Delivery & Feedback Loop (Optional Extension)
The meditation is surfaced:
- At the recommended time
- With minimal user interaction

After completion, the user may optionally provide a short reflection ("Helpful", "Too long", "Not needed"), which is stored and used by Gemini to refine future reasoning.

---

## Key Gemini 3 Features Used

### Gemini 3 Pro (Core Engine)
- Long-context reasoning across multiple calendar events
- Strategic decision-making (when, what, how)
- Contextual language generation
- Adaptive personalization

### Gemini Text Generation
- Situational meditation scripts
- Transition-aware language

### Gemini Audio Generation
- Dynamic speech synthesis
- Timing and pacing control

**Optional extension:** Gemini Live API for real-time adjustment during meditation

---

## Technical Architecture

### Frontend
- Web app (React / Next.js)
- Calendar visualization
- Audio playback UI

### Backend
- Google Calendar API (read-only)
- Gemini 3 API
- Lightweight session storage (no long-term data retention required)

### Flow
```
Calendar → Gemini reasoning prompt
Gemini strategy → script generation
Script → audio synthesis
Audio → web playback
```

---

## Scope Control (Solo-Friendly)

### Included
- Single-day calendar analysis
- 3–4 distinct meditation styles
- One voice
- One calendar integration
- Clear reasoning trace for demo

### Explicitly Out of Scope
- Mobile apps
- Full health analytics
- Mental health diagnosis
- Multi-voice libraries

---

## Safety & Framing

CalmSync is framed as a **well-being and focus support tool**, not a medical or mental health service. The app:
- Does not diagnose stress or anxiety
- Does not store sensitive health data
- Avoids therapeutic or clinical claims

---

## Demo Plan (3 Minutes)

### Minute 1
- Show a busy Google Calendar
- Explain how Gemini reasons about cognitive load

### Minute 2
- Trigger two different calendar scenarios
- Show two different meditation strategies and scripts

### Minute 3
- Play generated audio
- Highlight reasoning differences
- Emphasize autonomy and personalization

---

## Why This Project Stands Out

- Uses Gemini 3 as a **reasoning agent**, not a content generator
- Demonstrates **autonomy and decision-making**
- Integrates **multimodal generation** meaningfully
- Solves a real, relatable problem
- Clean, explainable demo within time limits

---

## One-Sentence Takeaway

> "CalmSync shows how Gemini 3 can reason about a user's real life and proactively generate meaningful interventions, rather than waiting to be prompted."

---

## Getting Started

*(Add installation instructions, API key setup, and usage guide here)*

## License

*(Add your chosen license here)*

## Contact

*(Add contact information or contribution guidelines here)*