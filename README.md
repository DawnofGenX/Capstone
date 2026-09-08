# Maze Runner — Single & Multiplayer Maze Game

A 2D maze game built with **Pygame**, featuring single-player and multiplayer modes over TCP sockets. Players navigate procedurally-themed mazes, collect coins and diamonds, avoid bombs, and race to the exit.

## Features

| Feature | Details |
|---------|---------|
| **Single Player** | Navigate mazes, collect items, avoid hazards |
| **Multiplayer** | Real-time 2-player over TCP sockets (host/join) |
| **Level System** | Multiple difficulty levels with increasing complexity |
| **Item System** | Coins, diamonds, bombs, free-to-play power-ups |
| **UI Screens** | Main menu, level select, settings, multiplayer lobby |
| **Animations** | Intro and page-transition video animations |

## Project Structure

```
Capstone/
├── capstone maze code.ipynb   # Main game logic (Pygame + socket networking)
├── Images/                    # Game assets (sprites, backgrounds, UI buttons)
│   ├── Back.png               # Navigation button
│   ├── Bomb.png               # Hazard item
│   ├── Coin.png               # Collectible
│   ├── Diamond.png            # Rare collectible
│   ├── Free_to_Play.png       # Power-up
│   ├── Levels.png             # Level select button
│   ├── MultiPlayer.png        # Multiplayer button
│   ├── Quit_Game.png          # Quit button
│   ├── Setting.png            # Settings button
│   ├── SinglePlayer.png       # Single player button
│   ├── Start.png              # Start button
│   └── background.png         # Menu background
├── Video_Animations/          # UI transition animations
│   ├── Intro_Page.mp4
│   ├── Levels_Page.mp4
│   ├── Main_Page.mp4
│   ├── Multiplayer_Page.mp4
│   └── SinglePlayer_Page.mp4
└── LICENSE                    # MIT
```

## How to Run

### Prerequisites

```bash
pip install pygame numpy matplotlib
```

### Run the Game

```bash
# From the notebook (Jupyter)
jupyter notebook "capstone maze code.ipynb"

# Or extract the code to a .py file and run directly
python maze_game.py
```

### Multiplayer Mode

1. **Host** starts the game and selects "Multiplayer" → "Host"
2. **Joiner** selects "Multiplayer" → "Join" and enters the host's IP address
3. Both players navigate their respective mazes in real-time

## Technical Notes

- **Rendering:** Pygame surface-based rendering at 60 FPS
- **Networking:** Python `socket` module for TCP multiplayer (host listens, client connects)
- **Game Loop:** Standard Pygame event-driven loop with state machine for screen transitions
- **Assets:** PNG sprites for all UI elements and game objects; MP4 animations for transitions

## License

MIT — see [LICENSE](LICENSE)
