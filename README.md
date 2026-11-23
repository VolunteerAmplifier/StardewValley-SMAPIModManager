<p align="center">
  <img src="https://i.postimg.cc/1z1Rw049/banner.png" alt="Stardew Valley SMAPI Mod Vault — 1-Click Mod Profile Switcher & Farm Save Backup" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Stardew%20SMAPI%20%26%20Save%20Vault-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-stardew--mods--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# Stardew Valley SMAPI Mod Vault — 1-Click Mod Profile Switcher & Farm Save Backup

**Playing a huge Stardew Valley Expanded solo farm with 60 mods, and also playing a vanilla or lightly-modded co-op farm with friends? Switch entire Mods folders in one click, scan SMAPI-latest.txt for broken mods, and back up your AppData farm saves safely.**

Stardew Valley SMAPI Mod Vault simplifies multi-profile modding on Windows: **managing named `Mods` profiles (`Expanded_Solo`, `Coop_Friends`, `Vanilla`), reading `manifest.json` versions, highlighting red errors from `SMAPI-latest.txt`, and archiving `%APPDATA%\StardewValley\Saves`**.

This project is aimed at **Stardew Valley (`1.6+`) on Windows 10/11 PC (Steam & GOG)** for switching mod setups cleanly without ruining co-op compatibility or losing multi-year farms.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Joining a friend's co-op farm fails because you have 50 solo mods active | Manually moving 50 folders out of `Stardew Valley\Mods` every session is tedious | Switch between **Expanded Solo** and **Co-op / Vanilla** profiles in 1 click |
| Red text in SMAPI console after a Stardew Valley 1.6 patch | Outdated `manifest.json` mods or missing Content Patcher dependencies | Scan `SMAPI-latest.txt` to list exact outdated/broken mods with Nexus IDs |
| Accidentally sleeping through a festival or corrupting a Year-4 farm | Stardew Valley keeps only current day and `_old` previous day save | Keep 25 rolling `.zip` snapshots of `%APPDATA%\StardewValley\Saves` |
| Installing a `.zip` mod into `Mods\` creates nested `Mods\ModName\ModName` | Double-nested folders prevent SMAPI from loading `manifest.json` | Drag-and-drop `.zip` mods to auto-flatten nested `manifest.json` folders |

## Download for Windows

[**Download StardewModVault.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/StardewModVault.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `StardewModVault.exe`? (Key features)

- Switches complete **Mod Profiles** (`Solo Expanded`, `Co-op`, `Vanilla`) in one click without redownloading anything.
- Drag-and-drop `.zip` mod installer automatically fixes double-nested folders so `manifest.json` sits at the right depth.
- Parses `%APPDATA%\StardewValley\ErrorLogs\SMAPI-latest.txt` to highlight skipped/broken mods in plain English.
- Creates timestamped `.zip` backups of `%APPDATA%\StardewValley\Saves` before launching modded sessions.

### Sample Output

```text
[StardewModVault] Active Profile: Stardew_Expanded_Solo (46 active mods)
[OK]   SMAPI Log Audit  : 0 errors | 1 update notice (Content Patcher 2.5.1 available)
[OK]   Farm Save Vault  : Backed up 'EmeraldFarm_38491024' (Year 3 Summer 14 -> 3.8 MB ZIP)
[INFO] Quick Switch     : Ready to swap to 'Coop_Vanilla_Light' (4 mods) in 1 click
```

The release ZIP is named `StardewModVault.zip`; the Windows executable inside is named `StardewModVault.exe`.

1. Close Stardew Mod Vault before updating or replacing executable files.
2. Click **Download StardewModVault.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `StardewModVault.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) with Stardew Valley and SMAPI installed.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `StardewModVault.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Effortless switching between Solo Modded and Co-op Farms

Prevents accidentally loading your massive solo modlist into a friend's co-op save.

### Auto-flattening nested `.zip` mod archives

Eliminates the #1 SMAPI mistake where `manifest.json` is buried one folder too deep.

### Plain-English `SMAPI-latest.txt` diagnostics

Extracts only the broken mods and missing dependencies from SMAPI's log file.

### Multi-season farm save history

Protects your farms beyond Stardew's single `_old` day backup.

## Default folders and configuration paths

Stardew Mod Vault manages `Stardew Valley\Mods` profiles and `%APPDATA%\StardewValley\Saves`:

```text
%APPDATA%\StardewValley\Saves\
```

Typical directory layout:

```text
Stardew Valley\
├── Mods\                 (Active profile mods)
└── _ModProfiles\
    ├── Expanded_Solo\
    └── Coop_Friends\

%APPDATA%\StardewValley\
├── Saves\                (Backed up to Documents\Stardew-FarmVault)
└── ErrorLogs\SMAPI-latest.txt
```

Always close Stardew Valley and the SMAPI terminal window before switching mod profiles or restoring a farm save.

## Quick start guide

Follow these steps to get started:

1. **Close Stardew Valley and SMAPI completely.** Extract `StardewModVault.zip` and launch `StardewModVault.exe`.
2. **Click **Back Up All Farms** to archive `%APPDATA%\StardewValley\Saves`.** Save your current `Mods` folder as a named profile.
3. **Create a second profile for **Co-op** or **Vanilla** and switch anytime in 1 click.** Drag new `.zip` mods onto the window for auto-flattened installation.

### Data safety note

Stardew Mod Vault preserves all profiles and farm backups cleanly without deleting mod configs.

## What the status summary shows

Stardew Mod Vault displays **active mod profile, loaded mod count, `SMAPI-latest.txt` error summary, and farm save backup path**.

## FAQ

**Does switching mod profiles delete my mod configuration files (config.json)?**

No—each profile preserves its own mod folders and `config.json` settings intact.

**How do I launch Vanilla Stardew Valley without SMAPI?**

Select the 'Vanilla' profile in Stardew Mod Vault and launch normally.

**Can I restore a farm from 5 in-game days ago?**

Yes—if you take snapshots in Stardew Mod Vault, you can restore any saved `.zip` point anytime.

## Useful reading

- [SMAPI Official Site — Stardew Modding API](https://smapi.io/)

## More Windows Gaming Utilities

- [ModDrop-UniversalPakInstaller](../ModDrop-UniversalPakInstaller) — Drag-and-drop ZIP/PAK mod installer with conflict check
- [BG3-ModPakLoadOrderSorter](../BG3-ModPakLoadOrderSorter) — Baldur's Gate 3 .pak mod load order & modsettings.lsx sorter
- [QuickSave-HotkeySnapshotVault](../QuickSave-HotkeySnapshotVault) — F5/F9 hotkey save snapshot & restore vault for any PC game
- [CloudSave-UniversalGameSync](../CloudSave-UniversalGameSync) — Automatic save folder synchronizer for non-Steam Cloud games

*Independent community project. Not affiliated with ConcernedApe, SMAPI, Valve, or Steam.*
