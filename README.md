# wonderous-soul-game


A 2D action Metroidvania written in Python with pygame, inspired by the style of Hollow Knight. Explore a connected underground world, fight bugs and bosses, unlock new abilities, and find your way to the final boss.

Everything is drawn with code (no image or audio files), and it all lives in a single file: `wonderous_soul.py`.

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

Press **Enter** on the title screen for a new game, or **C** to continue from your last save.

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
| Quit | Esc |

## How to play

- **Nail:** hit enemies with your nail to damage them and build up Soul.
- **Pogo:** strike downward in mid-air on an enemy or a spike to bounce off it and reset your air moves.
- **Focus:** stand still, hold F, and spend 33 Soul to heal one mask (health point).
- **Geo:** the currency dropped by enemies. Spend it with merchants.
- **Benches:** rest with W to restore health and set your respawn point. Resting also respawns regular enemies (defeated bosses stay down).
- **Death:** you respawn at your last bench and leave a shade holding your Geo where you fell. Strike the shade with your nail to get it back.
- **Doors:** some rooms have doorways. Press W at one to step through, since hidden areas are worth finding.
- **Gates:** some exits stay sealed until you defeat the boss guarding them.

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

Normal enemies include crawlers, flying insects, leaping hoppers, spitting plants, armored beetles, swooping bats, and ghosts that drift through walls. Three bosses block your progress: the **Husk Brute**, the **Crystal Weaver**, and the final boss, **The Warden**. After The Warden, a sealed gate opens into **The Abyss**, a generated underground of about 60 more rooms across four regions (Ashen Caverns, Glowmire Swamp, Bone Ruins, and Void Reach). Each region ends in a guardian boss, and the final boss waits at the bottom of the Void Reach. Defeat it to finish the game.

## Troubleshooting

- **`pip install pygame` fails with a long build error:** install `pygame-ce` instead, as shown above. Newer Python versions often have no prebuilt pygame package.
- **"Python was not found" on Windows:** install Python from [python.org](https://www.python.org/downloads/) and tick "Add python.exe to PATH", or use `py` instead of `python`.
- **"No such file" when running the game:** make sure your terminal is in the folder containing `wonderous_soul.py` (use `cd` to get there).
- **Window doesn't appear or the game runs slowly:** close other heavy programs and make sure your graphics drivers are up to date.

## Credits

Created with help from Claude (Anthropic). This is a fan-inspired project. It is not affiliated with or endorsed by Team Cherry, and it uses no assets from Hollow Knight. All art is generated in code.
