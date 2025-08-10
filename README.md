# Maze Game

A fun, fast-paced maze game built with **Python** and **Pygame**. Guide the player through three handcrafted levels before the timer runs out. Enjoy a starry animated menu, smooth 4‑directional movement, simple particle effects, and background music/SFX.

> University coursework by **Bahareh Heidarnezhad**.

## Requirements
- Python 3.10–3.12
- Pygame ≥ 2.5.2

Install Pygame directly:
```bash
pip install pygame
```

## How to Run
From the project root:
```bash
python -m src.maze_game
```
> Running as a module ensures imports like `from src.*` work and asset paths resolve from the repo root.

## Controls
- **W/A/S/D** or **Arrow Keys** — Move
- **Enter** — Confirm menu selection
- **Left/Right + Enter** — Choose on Game Over screen
- **Esc** — Back/Quit

## Project Structure
```
  README.md
  assets/images/over.png
  assets/images/player/player_down_0.png
  assets/images/player/player_down_1.png
  assets/images/player/player_down_2.png
  assets/images/player/player_down_3.png
  assets/images/player/player_left_0.png
  assets/images/player/player_left_1.png
  assets/images/player/player_left_2.png
  assets/images/player/player_left_3.png
  assets/images/player/player_right_0.png
  assets/images/player/player_right_1.png
  assets/images/player/player_right_2.png
  assets/images/player/player_right_3.png
  assets/images/player/player_up_0.png
  assets/images/player/player_up_1.png
  assets/images/player/player_up_2.png
  assets/images/player/player_up_3.png
  assets/images/tiles/finish.png
  assets/images/tiles/grass.png
  assets/images/tiles/wall.png
  assets/images/trophy.png
  assets/music/background.mp3
  assets/sounds/Fail.wav
  assets/sounds/win.wav
  src/__init__.py
  src/board.py
  src/create_player_sprites.py
  src/cut_spritesheet.py
  src/game_state.py
  src/levels.py
  src/map.py
  src/maze_game.py
  src/menu.py
  src/particles.py
  src/player.py
  src/sound_manager.py
```

### Important modules
- `src/maze_game.py` — app entry point
- `src/board.py` — gameplay loop, input, win/lose states, timer, rendering
- `src/menu.py` — animated start menu with level select
- `src/player.py` — movement and sprite animation
- `src/map.py` + `src/levels.py` — tile map + level data
- `src/particles.py` — lightweight particle effects
- `src/sound_manager.py` — music + SFX

## Notes
- Keep your working directory at the **repo root** when running the game so `assets/...` paths resolve.
- Fonts are loaded via `pygame.font.SysFont` which may vary across systems. If you want consistency, bundle a `.ttf` in `assets/fonts/` and switch to `pygame.font.Font`.
- **Sound files:** the code expects `assets/sounds/move.wav` and `assets/sounds/win.wav`. If your folder contains `Fail.wav`, rename it to `move.wav` (or update `src/sound_manager.py`).

## Notes on Assets
- All file paths in code assume the **project root** as the working directory.  
- Images and sounds in the `assets/` folder are **used for educational purposes only** and are not licensed for reuse or redistribution.  
- These assets are **not** covered under the same license as the source code. If you intend to publish or distribute this game, replace them with your own or properly licensed alternatives.  
---

Made with ❤️ using Python & Pygame.
