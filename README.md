# 🐜 Marabunta
**Ant Battle Simulator: A "Legacy Java vs. AI vs. Human" Experiment.**

I recovered a personal project from 2016 originally written in Java (Android Studio) and decided to bring it to the web. This repo is a side-by-side comparison of what happens when you let an AI port legacy code vs. when a human refactors it for a performance and features.

## 🚀 The Experiment
- **v1 (AI Baseline):** Core logic ported by Gemini from the original Java code. It works, but many features are missing. Also some bugs are present. [Play here](https://pablo-quilez.github.io/marabunta/v1/index.html)
- **v2 (Human Refactored):** Manually refactored and improved (logic, HUD, graphics, steering behavior, local avoidance, etc.). Added many features (e.g. Boss level) and logic. Optimized for thousands of active ants at 60 FPS. [Play here](https://pablo-quilez.github.io/marabunta/v2/index.html)

## 🕹️ How to play? (v2)

* **Click/Tap:** Command the black ant swarm. Attack red ants to survive.
* **[S] Key:** Mass spawn (Stress test your CPU).
* **[D] Key:** Debug mode (FPS & real-time execution stats).
* **[L] Key:** Toggle health indicators.

## 🛠️ Technical Highlights

* **GPU-Friendly Rotation:** Restricted ant angles to 5º steps (angle snap). This allows the browser to cache bitmaps instead of asking the GPU to re-render every single frame.
* **Grid-based Collisions:** Instead of checking every ant against every other ant, the map is divided into a grid. Massive performance boost. This allows to handle thousands of ants.
* **Dynamic FPS management:** Instead of lagging, if computer is heavy loaded, dynamically scales logic to maintain stability.
* **Local score:** Score is stored locally.
* **Basic enemy AI:** Based on distance to the nearest black ant. Red ants seek enemies inside its vision radius. If the population hits 1000+ ants, the AI logic scales back automatically to keep the framerate buttery smooth.

## ⚖️ License & Attribution
- **Code & Project:** [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.html). Free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation.
- **Graphics:** <a href="https://www.flaticon.com/free-icons/ant" title="ant icons">Ant icons created by Freepik - Flaticon</a>. Modified from <a href="https://www.flaticon.com/free-icon/ant_47288#term=ant&page=1&position=3">this one</a>.

## Contact
[LinkedIn](https://www.linkedin.com/in/pablo-quilez)