[Uploading README.md…]()

# Wonderous Soul

A 2D action Metroidvania written in Python with pygame, inspired by the style of Hollow Knight. Explore a connected underground world, fight bugs and bosses, unlock new abilities, and find your way to the final boss.

Everything is drawn with code (no image or audio files), and it all lives in a single file: `wonderous_soul.py`.

<!-- Add a screenshot or GIF here, for example:
![Gameplay](docs/screenshot.png)
-->

## Requirements

- Python 3.9 or newer
- `pygame-ce` (a maintained fork of pygame that works on current Python versions)

## Install and run

1. Download `wonderous_soul.py` and open a terminal in the folder where you saved it.
2. Install the dependency:

   ```
   pip install pygame-ce
   ```

3. Run the game:

   ```
   python wonderous_soul.py
   ```

On Windows, if `python` isn't recognized, use the `py` launcher instead:

```
py -m pip install pygame-ce
py wonderous_soul.py
```

On macOS/Linux you may need `python3` and `pip3`:

```
pip3 install pygame-ce
python3 wonderous_soul.py
```

Use the main menu to start a game: **Start** begins a new game in a save slot and **Continue** resumes your last one.

## Controls

| Action | Keys |
| --- | --- |
| Move | A / D or Left / Right arrows |
| Jump (hold for a higher jump) | Space or Z |
| Nail attack | X or J |
| Strike upward | Hold W or Up while attacking |
| Downward strike / pogo | Hold S or Down in mid-air while attacking |
| Dash (after finding the cloak) | C, Left Shift, or L |
| Focus (heal) | Hold F (needs 33 Soul) |
| Talk / use door / rest at bench | W or Up |
| Buy from a shop | 1, 2, 3 |
| World map | M |
| Charm menu (A/D to choose, Enter to equip) | I |
| Pause menu | Esc |

## How to play

- **Nail:** hit enemies with your nail to damage them and build up Soul.
- **Pogo:** strike downward in mid-air on an enemy or a spike to bounce off it and reset your air moves.
- **Focus:** stand still, hold F, and spend 33 Soul to heal one mask (health point).
- **Geo:** the currency dropped by enemies. Spend it with merchants.
- **Benches:** rest with W to restore health and set your respawn point. Resting also respawns regular enemies (defeated bosses stay down).
- **Death:** you respawn at your last bench and leave a shade holding your Geo where you fell. Strike the shade with your nail to get it back.
- **Doors:** some rooms have doorways. Press W at one to step through, since hidden areas are worth finding.
- **Gates:** some exits stay sealed until you defeat the boss guarding them.

## Charms

Ten charms can be found in the Abyss or bought from merchants. Each one costs one or two **notches**, and you start with 4. Every boss you defeat grants one more notch, up to 11. Press **I** to open the charm menu and choose which to equip, so you can tune your build:

| Charm | Effect |
| --- | --- |
| Heavy Nail | Much more nail damage |
| Quick Slash | Swing far faster |
| Soul Catcher | Extra Soul per hit |
| Fragile Heart | +2 max health |
| Swift Dash | Longer dash, faster recharge |
| Long Nail | Extended reach |
| Wind Stride | Run faster |
| Focused Mind | Focus heals in under half a second |
| Greed | 50% more Geo from enemies |
| Stone Skin | Stay invulnerable longer after a hit |

## Saving

The game saves automatically whenever you rest at a bench. The save is stored in `wonderous_soul_save.json` next to the game file. Delete that file to start fresh.

## Abilities

| Ability | What it does |
| --- | --- |
| Mothwing Cloak | Dash horizontally. Found in the first area. |
| Monarch Wings | A second jump in mid-air. Hidden in a shrine off the Fungal Gully. |
| Mantis Claw | Cling to walls and jump off them. Found on a high ledge past the Gully. |

Some routes are blocked until you have the right ability, so if you're stuck, look for what you haven't found yet.

## Upgrades and secrets

Merchants sell permanent upgrades for Geo: extra health, a sharper nail (more damage), faster Focus healing, and more Soul gained per hit. Extra health can also be found in a hidden vault and a hidden cellar holds a Geo cache.

## Enemies and bosses

Normal enemies include crawlers, flying insects, leaping hoppers, spitting plants, armored beetles, swooping bats, and ghosts that drift through walls. Three bosses block your progress: the **Husk Brute**, the **Crystal Weaver**, and the final boss, **The Warden**. After The Warden, a sealed gate opens into **The Abyss**, a generated underground of about 60 more rooms across four regions (Ashen Caverns, Glowmire Swamp, Bone Ruins, and Void Reach). Enemies get tougher and hit harder the deeper you go. Each region ends in a guardian boss, and the final boss waits at the bottom of the Void Reach. The final boss is **The Seraph**, a colossal angelic being that floats in the background. Watch for the warning beams before its lightning strikes, and strike the glowing sigil on its giant hands when they slam down and rest on the ground. Defeat it to finish the game.

## Running the tests

The tests run without a window (pygame is stubbed out), so they work anywhere:

```
pip install pytest
pytest -q
```

You can also run `python tests/test_game.py` directly.

## Troubleshooting

- **`pip install pygame` fails with a long build error:** install `pygame-ce` instead, as shown above. Newer Python versions often have no prebuilt pygame package.
- **"Python was not found" on Windows:** install Python from [python.org](https://www.python.org/downloads/) and tick "Add python.exe to PATH", or use `py` instead of `python`.
- **"No such file" when running the game:** make sure your terminal is in the folder containing `wonderous_soul.py` (use `cd` to get there).
- **Window doesn't appear or the game runs slowly:** close other heavy programs and make sure your graphics drivers are up to date.

## Contributing

Bug reports, ideas and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for how the code is organized and how to add rooms, monsters and charms, and [CHANGELOG.md](CHANGELOG.md) for the version history.

## License

Released under the [MIT License](LICENSE).

## Credits

Created with help from Claude (Anthropic). This is a fan-inspired project. It is not affiliated with or endorsed by Team Cherry, and it uses no assets from Hollow Knight. All art is generated in code.
