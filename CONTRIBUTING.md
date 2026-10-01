[CONTRIBUTING.md](https://github.com/user-attachments/files/32936796/CONTRIBUTING.md)
# Contributing to Wonderous Soul

Thanks for your interest! Bug reports, ideas and pull requests are all welcome.

## Getting set up

```
git clone <your fork url>
cd wonderous-soul
pip install -r requirements.txt pytest
python wonderous_soul.py
pytest -q
```

Please run the tests before opening a pull request. They run headlessly, so no window is needed.

## How the code is organized

Everything lives in `wonderous_soul.py`, in this order:

1. **Constants, settings and save helpers** - screen size, save slots, difficulty, controls/credits/changelog text.
2. **World data** - `mkroom()`, the hand-built `ROOMS`, NPCs and doors, `LINKS` (how rooms connect) and `MAP_POS` (map layout).
3. **Charms and the Abyss generator** - `CHARMS`, `REGIONS` and `gen_world()`, which appends about 60 generated rooms.
4. **Physics and entities** - `Body`, `Player` and `Enemy` (including each monster's AI and the Seraph's boss logic).
5. **Art** - textures, the cape, the player, monsters, NPCs, bosses. All art is drawn in code.
6. **`Game` class** - the update loop, interaction, menus, drawing and the main `run()` loop.

## Recipes

**Add a room.** Create it with `mkroom(...)` and add it to `ROOMS`. Then connect it by adding entries to `LINKS` (both directions) and a position to `MAP_POS`. A room needs an open side wherever it links to another room.

**Add a monster.** Add its stats to `Enemy.STATS`, a branch in `Enemy.update`, a draw function, and an entry in `DRAWERS`. Then place it in a room's `spawns`.

**Add a charm.** Add it to `CHARMS`, hook its effect where it applies (for example damage in `hit_enemy`), and place it as an item named `charm:<key>` or sell it in a shop as `charm:<key>`.

**Add a setting.** Add a default to `DEFAULT_SETTINGS`, a row in `settings_rows()`, and handle it in `change_setting()`.

## Pull requests

- Keep changes focused and describe what you changed and why.
- Add or update a test in `tests/test_game.py` when you change world data or game logic.
- The game uses no external art or sound files, so please keep contributions original and avoid assets from other games.
