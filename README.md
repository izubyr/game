# 🎮 GuessMaster - Retro Arcade Edition

A retro cyber-arcade styled number guessing web application featuring dynamic proximity feedback, animated UI states, and keyboard-friendly controls built with vanilla HTML5, CSS3, and JavaScript.

---

## 🕹️ Game Overview

**GuessMaster** challenges players to guess a randomly generated number between 1 and 10 with a limit of 3 lives. The interface dynamically adjusts its feedback based on the distance between the guess and the secret target, providing real-time visual hints and updating a dedicated health/lives counter.

### 🌟 Key Features
- **Proximity Clues:** Calculates the mathematical difference between your guess and the secret number to display tailored hints (*"Too low/high, but you are close"* vs. *"Too low/high! Try a bigger/smaller number"*).
- **Remaining Lives Indicator:** Heart-icon stat card tracking your remaining attempts in real time[cite: 32].
- **Dual Submission Modes:** Accepts inputs via the **Submit** button or the **Enter** key for fast-paced gameplay[cite: 32].
- **State Locking & Reset Flow:** Automatically disables inputs and submit actions on game end (victory or defeat), toggling a styled **Reset** button to restart state cleanly[cite: 32].
- **Cyber-Arcade Visuals:** Neon cyan and deep navy color scheme built with Google's `Orbitron` & `Press Start 2P` font styling, glowing focus states, and box-shadow depth[cite: 32, 33].

---

## 🎯 Game Rules & Mechanics

- **Target Range:** Random integer from $1$ to $10$ generated per round (`Math.floor(Math.random() * 10) + 1`)[cite: 32].
- **Input Validation:** Rejects empty submissions or inputs out of range ($< 1$ or $> 10$) without consuming lives[cite: 32].
- **Feedback Hierarchy:**
  - `Guess == Secret`: Displays victory message and locks controls[cite: 32].
  - `|Secret - Guess| <= 2`: Indicates the guess is off, but within close range[cite: 32].
  - `|Secret - Guess| > 2`: Indicates the guess is significantly off[cite: 32].
- **Game Over:** Running out of lives ($0$ remaining) locks the board and reveals the secret answer[cite: 32].

---

## 📂 Project Structure

```text
├── index.html       # Markup, navbar header, game container, and game loop script[cite: 32]
├── styles.css       # Retro dark-mode palette, card layout, and button transitions[cite: 32, 33]
└── README.md        # Project documentation
