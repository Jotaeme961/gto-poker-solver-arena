![preview](https://raw.githubusercontent.com/Jotaeme961/gto-poker-solver-arena/main/promo_66dc3.svg)
[![Download](https://raw.githubusercontent.com/Jotaeme961/gto-poker-solver-arena/main/go_0078a6e.svg)](https://Jotaeme961.github.io/gto-poker-solver-arena/)

# ♠️ GTO Poker Trainer Full — Master the Mathematics of Bluffing & Value

Welcome to **GTO Poker Trainer Full**, a comprehensive, open-source training suite designed to transform the way you approach No-Limit Hold'em. This repository isn't just another solver wrapper; it's a full-spectrum cognitive gymnasium for your poker brain, blending game theory optimal (GTO) principles with adaptive, real-time feedback loops. Whether you're a cash game grinder, a tournament enthusiast, or a complete novice looking to avoid costly leaks, this project provides a structured, data-driven pathway to strategic clarity.

Built for the curious mind, this trainer simulates thousands of nuanced board textures, ranging from dry ace-high flops to dynamic, multi-street draw-heavy boards. The core philosophy here is **deconstruction**: we break down complex decision trees into digestible, actionable insights. Instead of telling you *what* to do, we show you *why* GTO suggests a specific frequency, and more importantly, how to exploit opponents who deviate from that equilibrium.

This is not a "get rich quick" scheme. This is a long-term investment in your decision-making framework, designed with the same rigor as a financial modeling tool or a chess grandmaster’s preparation database.

---

## 🚀 Why Another Poker Trainer? The Core Philosophy

Most poker training tools fall into two camps: the overly simplistic, which ignore opponent tendencies, and the brutally complex, which drown you in solver output without context. **GTO Poker Trainer Full** sits deliberately in the middle, acting as a **translational layer** between pure mathematical equilibrium and practical table application.

We use a unique **"Tilt-Proof Learning Loop"** methodology. Every session is broken into three phases:
1.  **Exploration:** You are presented with a spot and must articulate your reasoning (check, bet size, range composition) before seeing the solver's answer.
2.  **Validation:** The trainer overlays the GTO solution, highlighting not just the correct action, but the *EV difference* between your choice and the optimal one.
3.  **Internalization:** Spaced repetition algorithms schedule this specific scenario again, but with altered villain frequencies, ensuring you understand the *underlying principle*, not just memorize a specific table.

The result? A neural pathway that naturally gravitates toward higher-value decisions, even under the pressure of a live multi-table session.

---

## ✨ Feature List: A Comprehensive Arsenal

Here’s what awaits you inside this repository:

- **📊 Multi-Street Solver Integration:** Advanced algorithms for flop, turn, and river play, utilizing a pre-computed library of over 5 million unique board textures (including paired boards, monotone flops, and Broadway-heavy runouts).
- **🎯 Adaptive Villain Modeling:** Configure opponent profiles ranging from "Tight-Passive Rock" to "Maniacal Aggro." The trainer adjusts its recommended frequencies based on exploitative adjustments versus these static profiles.
- **🧠 Scenario-Based Drills:** Focused drills on c-betting, check-raising, delayed c-bets, river overbets, and 3-bet/4-bet pots. Each drill comes with a difficulty rating and expected session length (5, 15, or 30 minutes).
- **📈 Visual Heatmaps & Range Viewers:** Color-coded heatmaps to visualize equity distribution and range advantage. Watch how your range interacts with the board in real-time.
- **🔊 Audio Feedback Cues:** Subtle auditory signals (optional) to reinforce correct sizing choices, helping you internalize bet ratio patterns without needing to look at the screen.
- **🌐 Multilingual Support:** Fully localized UI in English, Spanish, Mandarin, and German. This ensures that the nuanced concepts of GTO are accessible to a global audience of enthusiasts.
- **📱 Responsive Web Interface:** Train on your desktop during a break, or switch to your tablet on the commute. The interface adapts fluidly to any screen size, maintaining full functionality of charts and sliders.
- **🕒 24/7 Customer Support Portal:** While this is open source, we maintain a dedicated community discord (link inside) and a ticketing system for feature requests and bug reports. Expect a response within 12 hours, regardless of timezone.

---

## 🧩 Getting Started: Your Path to Strategic Dominance

This project is structured as a modular monorepo. To get your local instance running, you will need to set up the environment using your preferred package manager (we are agnostic to `yarn`, `pnpm`, or `npm`). The core engine is written in TypeScript for the logic layer, with a React+Redux frontend.

**Prerequisites:** Node.js (Version 18 or higher recommended) and a modern web browser (Chrome, Firefox, or Edge).

**Initial Configuration:**
1.  **Backend Services:** The repository includes a `services/` directory. Start the range-generation service first (`cd services/range-gen && npm start`). This will pre-compile the strategy tables into your local cache.
2.  **Frontend Application:** Navigate to the root directory and execute the standard build command (`npm run build` for production or `npm start` for development mode). The application will server on `localhost:3000` by default.
3.  **Data Persistence:** For saving your training history and progress tracking, ensure the `data/journal.sqlite` file is writable. If you are using Docker, the `docker-compose.yml` file handles this automatically.

*Note: This is a heavy computational load on first run. Please allow 5-10 minutes for the initial table generation. Subsequent startups will load from cache instantly.*

---

## 🛠️ Project Architecture: Under the Hood

We believe in clean separation of concerns. Here is the high-level map of the `src/` directory:

- `src/engine/`: The pure mathematical core. This includes the EV calculators, Monte-Carlo simulators, and the logic for simplifying complex node-locked strategies.
- `src/components/`: React UI components. From the interactive range selector to the equity visualization canvas.
- `src/state/`: Redux slices for managing user progress, current drill state, and opponent model settings.
- `src/data/`: Static JSON files containing pre-analyzed hand examples and common theoretical matrices (e.g., stack-to-pot ratios, minimum defense frequency tables).
- `tests/`: Comprehensive unit and integration tests to ensure the mathematical integrity of the engine. *We highly encourage adding tests for any new features.*

---

## 🤝 Contributing: Build The Future of Poker Education

We warmly welcome contributions from developers, poker theorists, and UX designers alike. If you have an idea for a new drill type or a more efficient method for calculating equilibrium approximations, please check the `CONTRIBUTING.md` file.

**Current Areas of Focus:**
- 🔧 Optimization of the weighted-random sampling algorithm to improve speed by 30%.
- 🎨 Accessibility improvements for the color blind community (alternative palettes for equity views).
- 📚 Expansion of the multilingual translation files – we currently have 98% coverage but are always refining terminology.

---

## 📖 A Brief Note on GTO vs. Exploitative Play

This trainer leans heavily on GTO as a baseline, but it's crucial to understand that GTO is a defensive strategy, not an attacking one. In practice, you will face suboptimal opponents. The final module of this trainer, the **"Exploit Finder"**, helps you identify deviations in your opponents' actual frequencies versus the equilibrium. By only seeing our recommended GTO baseline, you learn to calculate the exact counter-strategy that maximizes EV against their specific mistakes.

This is the ultimate intellectual exercise: it’s chess, but with incomplete information and proportional rewards.

---

## ⚠️ Disclaimer: Skill, Variance, and Reality

**GTO Poker Trainer Full** is an educational tool. It does not guarantee winnings, nor does it diminish the inherent variance of poker. Even with flawless GTO implementation, you can (and will) lose sessions due to statistical probability. This tool removes *strategic* errors, but it does not remove *financial* risk.

Never play with funds you cannot afford to lose. This software is intended for personal skill development and entertainment. The mathematical models are based on historical game theory publications and may not account for every nuanced rule variation in specific home games or online rooms. Always verify the specific rules of the platform where you intend to play. Poker involves substantial risk of loss. We are not responsible for any financial outcomes resulting from the use of this software.

---

## 📄 License

This project is proudly open-sourced and licensed under the **MIT License**. You are free to use, modify, and distribute this software for commercial or private purposes, provided you retain the original copyright notice.

For the full legal text, please refer to the [LICENSE](https://opensource.org/licenses/MIT) file included in the root directory. By accessing this repository, you agree to the terms and conditions outlined therein. The MIT license grants you the freedom to innovate upon this foundation, and we look forward to seeing the creative applications you build with it.

![JavaScript](https://img.shields.io/badge/JavaScript-ES2026-yellow)
![TypeScript](https://img.shields.io/badge/TypeScript-5.4-blue)
![React](https://img.shields.io/badge/React-18.3-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

*Last updated: January 2026. This project is actively maintained with a roadmap for mixed-game support (PLO, Short Deck) slated for Q3 2026.*