#the site is live at https://pks0408.github.io/zork-mumbai-2026-adventure/
# 🕹️ Project Zork: Mumbai 2026
**Developer:** Prabhav Kumar Sahu
**Institute:** Rajiv Ganghi Institute of Technology 
**Challenge:** Dev Club AI Challenge 2026  
**Tech Stack:** Gemini 2.5 Flash + Vanilla JS + CSS3 (CRT Shader)

---

## 🏛️ The Legacy: Reimagining Zork I (1980)
This project is a modern reconstruction of **Zork I: The Great Underground Empire**, originally released by Infocom in 1980. Zork was a pioneer of the "Interactive Fiction" genre, relying entirely on text and player imagination to explore a vast, hidden world.

### Then vs. Now:
* **The Parser:** While the 1980 original used a revolutionary 900-word parser, **Mumbai 2026** uses **Gemini 2.5 Flash**, allowing it to understand natural language, sarcasm, and complex intent.
* **The World:** Zork I featured a static map of 400 locations. Our version uses **Procedural World Building** to generate an infinite, evolving Mumbai ruins based on your specific actions.
* **The "Grue":** We have preserved the classic "Dread" mechanic—just as Zork players feared the dark, our engine tracks an internal `Dread` variable that makes the AI's descriptions more perilous as it rises.

---

## 🧠 Technical Innovation: The "State-Aware" Engine
The core innovation is the bridge between **Generative AI** and **Programmatic UI**:

1. **State-Listening via Regex:** The engine uses Regular Expressions to "sniff" the AI's output for `[STATUS]` tags (Health/Dread). This allows the frontend to react to the AI's internal logic.
2. **Dynamic Visual FX:** - **Damage Shake:** When the AI reduces player health, a CSS `shake-screen` animation is triggered.
   - **Critical Pulse:** If health drops below 30%, the terminal initiates a red pulse effect to signify danger.
3. **Throttled Persistence:** To respect Gemini's free-tier rate limits, I implemented a 10-second "Safety Buffer" and **Exponential Backoff** logic. This ensures the game remains stable even during high-traffic demo sessions.

## 🎨 Retro-Futuristic UI
I built a **CRT Terminal Emulator** using custom CSS to capture the 80s aesthetic:
* **Scanline Shader:** Mimics 80s tube monitors using linear-gradient overlays.
* **Neural Flicker:** A subtle opacity animation simulating hardware voltage instability.
* **Phosphor Green:** An authentic high-contrast palette optimized for the post-apocalyptic aesthetic.

---

## 🎮 Gameplay Mechanics
* **Procedural Mumbai:** Explore the ruins of the Gateway of India, Colaba, and local BEST buses in a gritty 2026 setting.
* **Survival Tracking:** - **Health:** Managed by the AI. Reaching 0% results in a "Neural Link Severed" (Game Over).
   - **Dread:** An atmospheric variable that influences the darkness of the AI's descriptions.
* **Infinite Replayability:** No two games are the same. The AI adapts to your specific commands, from searching for supplies to attempting to use pre-apocalypse technology.

---

## 👤 Developer
**Prabhav Kumar Sahu** – CSE RGIPT 

Built for the Dev Club AI Challenge 2026.
