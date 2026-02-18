
# Flappy Bird — LÖVE2D Edition (CS50G Inspired)
A modern take on the classic **Flappy Bird** game built using **Lua** and **LÖVE2D** (Love2D).

Test your reflexes and see how far you can fly through the pipes!

With increasing difficulty and score-based medals, every run is a challenge.

---

## 🎮 Game Overview
Inspired by **CS50’s Introduction to Game Development**, this Flappy Bird remake features:

- Smooth physics for the bird
- Procedurally generated pipes with gaps
- Score tracking system
- Sound effects for jumps, collisions, and scoring
- End-game medal display based on your performance
- Nostalgic pixelated font style

### Gameplay
![Gameplay - Screenshot](/Flappy%20Bird%20-%20Gameplay.png)
![Score Page - Screenshot](/Flappy%20Bird%20-%20Score%20Page.png)

**How it works:**

- Press a key to make the bird "jump".
- Avoid pipes and the ground.
- The game ends if the bird hits a pipe or the ground.
- Your score is the number of pipes successfully passed.
- At the end, a medal is displayed depending on your score:

| Medal | Score Requirement |
|---|---|
| Gold | 20 |
| Silver | 10 |
| Bronze | 5 |

---

## 🧰 Requirements
To play this game, you’ll need:

- **Lua 5.1 or later**
- **LÖVE2D (Love2D)** game framework

---

## ⚙️ Installation Guide
### Step 1: Install Lua
1.  Go to [https://www.lua.org/download.html](https://www.lua.org/download.html)
2.  Download the latest version for your OS.
3.  Follow the installation instructions for your platform.

> 🪟 **Windows Tip:**
> You can also install Lua easily using [Lua for Windows](https://github.com/rjpcomputing/luaforwindows/releases).

### Step 2: Install LÖVE2D
1.  Visit [https://love2d.org/](https://love2d.org/)
2.  Download and install the version for your OS.
3.  Verify installation by running in terminal:
    ```bash
    love --version
    ```
If a version number appears, installation is successful.

💡 **Adding to PATH (if necessary):**

-   **Windows:** Reinstall Love2D and select “Add to PATH”
-   **macOS:** Should work automatically
-   **Linux:** Use your package manager, e.g., `sudo apt install love`

### Step 3: Download the Game
**Option A: ZIP Download**

1.  Click “Code” → “Download ZIP” on the repository
2.  Extract the ZIP anywhere
3.  Ensure files like `main.lua`, `Bird.lua`, `Pipe.lua` are present

**Option B: Git Clone**

	git clone [https://github.com/yourusername/flappy-bird.git]
	cd flappy-bird

### Step 4: Run the Game
From the game folder (where `main.lua` is located), run:

`love .`

The game window will open, and you’re ready to play!

---

## 🕹️ Controls
| Key | Action |
|---|---|
| `Space` | Make the bird jump |
| `Enter` | Start / Restart the game |
| `Esc` | Quit the game |

---

## 🧠 How It Works
The game uses a state machine:

-   `TitleScreenState`: Shows the start screen
-   `CountdownState`: Countdown before game starts
-   `PlayState`: Main gameplay
-   `ScoreState`: Displays final score and medals

### Gameplay Mechanics:

-   Bird physics is simulated using gravity and jump force
-   Pipes move towards the bird with randomized gaps
-   Each successfully passed pipe increases your score
-   The end screen displays a medal based on your performance

### Technical Aspects

-   **Sound Assets (`/sounds`):**
    -   `jump.wav` — Bird jump
    -   `hurt.wav` — Bird collision
    -   `explosion.wav` — Bird hit ground
    -   `score.wav` — Pipe passed
    -   `marios_way.mp3` — Background music
-   **Icons (`/icons`):**
    -   `gold_medal.png`, `silver_medal.png`, `bronze_medal.png` — End-game medals
-   **Graphics & Fonts:**
    -   `bird.png`, `pipe.png`, `background.png`, `ground.png`
    -   `flappy.ttf`, `font.ttf` — Retro pixel fonts
-   **Core Logic Files:**
    -   `main.lua` — Entry point
    -   `Bird.lua` — Bird physics & rendering
    -   `Pipe.lua` — Single pipe
    -   `PipePair.lua` — Pair of pipes
    -   `class.lua` — Class helper
    -   `StateMachine.lua` — Game state handling
    -   `BaseState.lua` & other states — Game states

---

## Reference
[CS50's Introduction to Game Development - Week 1](https://cs50.harvard.edu/games/weeks/1/)
