# Bloobs Adventure Idle Save Editor [aka BAI Save Editor]

Powerful save editor for Bloobs Adventure Idle. It is built for power users, but the UI is designed to be approachable for beginners: load a save, edit values, review changes, keep backups, and write the save safely.

## Download
-Download the latest Release.

-Extract the ZIP somewhere convenient, such as your Desktop or Downloads folder.

-Run: BAI Save Editor.exe

-Since the app is unsigned, you may receive a SmartScreen warning. Click “More Info” -> “Run Anyway.”

## What It Can Do?

- Auto-detect the game install, save folder, save slots, and Unity game data.
- Edit `SaveFile.es3` and supported future save slots.
- Edit gold, quest points, skills, XP, multipliers, inventory, bank, equipment, challenges, collections, settings, and raw ES3 keys.
- Browse a local item catalog extracted from the installed game files, including item images where available.
- Add items to inventory or bank from the catalog.
- Edit saved item stats, requirements, quantities, values, and custom fields.
- Use the Wiki tab for local item, recipe, drop, stat, and crafting information extracted from the game itself.
- Preview unsaved changes and validation warnings before saving.
- Create automatic backups before writing saves and restore backups from the app.
- Keep `IsModded=false` by default, while still allowing users to preserve or force the flag if they choose.
- Auto-scan schema/catalog data on startup and refresh when the game updates.

Note: Every time you open Save Editor, a 2-3 minute scan runs. For now, this is necessary to ensure you get the most up-to-date values, even if the game is updated. If I find a better method, I’ll change it.

## Game Stat Patch

Some item stats are reset by the game on load from its built-in item database. The editor includes an optional "Game Stat Patch" that makes saved item stat edits survive game load for inventory, bank, and equipment items. (Yes, you can max out equipment/item stats to 999!)

The patch:

- Backs up `Assembly-CSharp.dll` before changing it.
- Removes the game code that overwrites saved item stats with canonical item asset values.
- Can be checked, enabled, or restored from the Actions tab.

After a game update, run "Actions -> Game Stat Patch -> Check" and enable it again if needed.

## Safe Use

1. Close Bloobs Adventure Idle before saving or patching.
2. Open the editor and let it auto-scan.
3. Load your save slot.
4. Make edits.
5. Review unsaved changes and warnings.
6. Save. The editor creates a backup automatically.

If something goes wrong, use the Backups tab to restore an earlier save.

## Notes

- The local Wiki and item catalog come from your installed game files, so they are usually more current than old online guides.
- Patching game files is optional. Save editing works without it, but some non-HP item stat cheats may be reset by the unpatched game.
- Steam/game updates may replace patched files. Re-check patch status after updates.
- Feel free to report any bugs/issues and improvement ideas!
