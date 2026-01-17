# 🦠 The Glitch Gardener

> **"Don't fix the system. Cook it."**

**The Glitch Gardener** is a reverse-bullet-survivor game set on a chaotic Windows 95 desktop. You don't play as the hero defending the computer—you play as the **Virus**.

Developed solo by **Studio Raaav** for the **Brainwave 2.0 Game Jam**.

---

## 🎮 Gameplay Loop & Objective
The genre is usually about defending yourself, but here, you are the threat.
* **The Goal:** **Survive for 2 Minutes 30 Seconds.**
* **The Win Condition:** Stay alive until the timer hits `00:00` to successfully crash the system (Blue Screen of Death).
* **The Lose Condition:** If your **System Integrity (Health)** reaches **0%** before the timer runs out, the Antivirus deletes you. Game Over.

---

## 🎨 Jam Themes Implemented

This game was built to fit specific themes provided during the offline round:

### 1. ⏳ "The End is Near"
* **Interpretation:** Usually, a countdown signifies a "Game Over" or failure. In *The Glitch Gardener*, the end of the timer is your **Victory Condition**.
* **Implementation:** As the clock ticks down, the environment becomes more hostile, lights turn red, and the music accelerates. You are racing *towards* the end.

### 2. 👾 "Glitches are Intentional"
* **Interpretation:** Instead of bugs being annoying errors, they are features.
* **Implementation:**
    * **System Lag Zone:** A weaponized glitch that drops FPS (intentionally) to slow down enemies by 75%.
    * **Pop-up Blockers:** Used as physical shields to block Antivirus attacks.

---

## 🕹️ Controls

| Key | Action |
| :--- | :--- |
| **W, A, S, D** | Move the Virus |
| **Left Click** | **Glitch Blade** (Swipe Attack) |
| **E** | Open **Dark Web Shop** (Buy Upgrades) |
| **Esc** | Pause Game |

---

## 🛠️ Technical Highlights (Under the Hood)

### ⚡ The "Hit Stop" Mechanic
To give the melee combat weight without using projectiles, I implemented a **0.1s Screen Freeze** on every kill.
* *Challenge:* Using `Time.timeScale = 0` caused an infinite loop bug where the un-pause coroutine never fired.
* *Solution:* Implemented `WaitForSecondsRealtime` to bypass the game loop and ensure the "crunch" feel works perfectly without crashing the logic.

### 📉 System Lag Zones
A custom area-of-effect system that modifies enemy script variables (`Speed`) in real-time when they enter specific Trigger Colliders tagged `lagzone`.

## 🚀 Installation & How to Play
1.  Download the latest build from https://studioraaav.itch.io/the-glitch-gardener.
2.  Unzip the folder.
3.  Run `TheGlitchGardener.exe`.
4.  **Warning:** May cause nostalgia for 1995.

---

## 👨‍💻 Credits
* **Developer:** Studio Raaav (Solo Dev)
* **Engine:** Unity (2D / URP)
* **Event:** Brainwave 2.0 Game Jam (Offline Round)

---
*Made with ❤️ by Studio Raaav*
