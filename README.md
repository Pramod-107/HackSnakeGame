# HackSnake

A feature-rich **Snake game** built using the **Jack language** for the **Nand2Tetris** project. This version introduces advanced mechanics like shrinking obstacles, time-sensitive bonus food, and a high-score system, all running on the Hack computer architecture.

## Features

* 🍎 **Dynamic World Generation** – Food, special bonuses, and obstacles are spawned at random coordinates using a custom pseudo-random number generator.
* ⚡ **Special Food & Timers** – "Big Food" spawns every 5 seconds at random locations, offering bonus points if collected quickly.
* ⚠️ **Strategic Obstacles** – Hitting an obstacle doesn't kill you instantly; instead, it subtracts points and **shrinks** your snake, adding a layer of strategy.
* 🏆 **High Score System** – Persistent tracking of the session's high score with dynamic on-screen updates.
* 💾 **Optimized for Hack** – Implements a history-rewriting algorithm to manage memory efficiently for the snake's body coordinates.

## How to Play

1. **Load the Game:** Open the **Nand2Tetris VM Emulator** and load the `bin` folder containing the compiled `.vm` files.
2. **Settings:** Set the animation speed to **No Animation** (or Fast) for the best gameplay experience.
3. **Controls:** Use the **Arrow Keys** to steer the snake.
4. **Scoring:**
   * **Normal Food (Small Circle):** +1 Point & Growth.
   * **Special Food (Big Circle):** +5 Points (Despawns every ~5 seconds).
   * **Obstacle (Square):** -1 Point & Shrinks the snake.
5. **Game Over:** Avoid hitting the walls or your own tail!

## Implementation Details

* **Jack Language** – The entire game logic, rendering, and input handling are written in high-level Jack code.
* **Collision Handling** – Custom logic prevents 180-degree turns and handles complex collisions between the snake head and various board elements.
* **Memory Management** – Uses a cyclic buffer approach to rewrite the snake's movement history, preventing stack overflow during long playthroughs.
* **Visual Optimization** – Explicit screen clearing ensures score updates don't leave "ghost" characters on the display.

## 📂 Project Structure

```text
/HackSnake
│── /src          # Jack source files (.jack)
│── /bin          # Compiled VM files (.vm)
│── README.md     # Project overview
