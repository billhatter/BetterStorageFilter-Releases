# Better Storage Filter — downloads

Binary releases and supporting documentation for **Better Storage Filter**, a RogueTech-required ModTek mod for **HBS BATTLETECH → MechBay → Storage**. This is not the post-mission salvage screen and is not a vanilla-game mod.

### This mod was programmed using AI. Although a Sr. Software Engineer w/over 25yrs of experience, I chose to use Codex as my programming tool while I did design, architecture, QA, and all final decisions. All code went through a minimum 3 independent agent reviews as well as human review. AI was ONLY used for programmatic work for expedience and overcoming challenges hooking into the game.
### While this version of the mod was designed and written for RogueTech, the RogueTech team is neither responsible for, nor will they in any way support, Better Salvage Filter.
### Use of this mod with RTO WILL get you banned for cheating.

This repository contains **downloads, checksums, release metadata and user documentation only**. Project source and development history are not published here.

## Download 0.2.0 (beta)

- **[Vortex installer: BetterStorageFilter-0.2.0-vortex.zip](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/BetterStorageFilter-0.2.0-vortex.zip)** — drop into Vortex or use Install From File.
- [Manual download: BetterStorageFilter-0.2.0-mvp.zip](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/BetterStorageFilter-0.2.0-mvp.zip) — the original manual ModTek ZIP.
- [SHA-256 checksums](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/SHA256SUMS.txt)
- [Release metadata and payload hashes](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/release-info.json)
- [Release page](https://github.com/billhatter/BetterStorageFilter-Releases/releases/tag/v0.2.0)

Both ZIPs contain the **same tested 0.2.0 mod files and DLL**. The Vortex ZIP adds only installation metadata selecting the correct game-folder destination. GitHub's automatically generated **Source code** ZIP/TAR files contain this download-page repository, not the mod or its implementation.

## Features

- Five independent type toggles: Mechs, Vehicles (ground), Battle Armor, VTOLs and ProtoMechs.
- Four independent weight toggles: Light, Medium, Heavy and Assault.
- Choices combine within each row; the type and weight rows intersect.
- All nine toggles start ON. **Reset Filters** enables them all.
- Turning every toggle OFF in either row shows no matches; OFF buttons remain clickable.
- Complete stored units and parts share the filters; selections are kept in runtime memory, not campaign-save data.
- Existing CustomFilters virtualization and the provider-owned IRTweaks Alt bulk-scrap workflow are retained.

## Requirements

An existing compatible **RogueTech** installation with **ModTek**, **RogueTech Core**, **CustomUnits**, **CustomFilters** and **IRTweaks**. Dependencies and game DLLs are not bundled. This is not a vanilla BATTLETECH mod. RogueTech updates can change compatibility or remove local mods.

## Install

### Vortex 1.14+

1. Close BATTLETECH and the RogueTech launcher/updater before deployment. Back up an existing manual `Mods/BetterStorageFilter` folder and avoid competing manual/Vortex copies.
2. In Vortex, manage **BATTLETECH** and verify its game location is the intended RogueTech installation.
3. Download **BetterStorageFilter-0.2.0-vortex.zip** above and drop it into the **Mods** archive area, or choose **Install From File**.
4. Check that **Mod Type is Engine Injector**, enable the mod, then **Deploy Mods**. This is Vortex's game-root deployment category; the package does not install `dinput8.dll` or replace an engine hook.
5. The resulting location must be `<game>/Mods/BetterStorageFilter/mod.json` next to `BetterStorageFilter.dll`, **not** the Documents mod folder. If the type/destination is wrong, stop before deployment and check your Vortex version/archive.

**Nexus Collections are not supported by this override-based package:** Vortex ignores the override instructions while installing collection dependencies. Use normal Install From File. No separate installer app, extension or Vortex restart is required.

### Manual installation

1. Close the game and launcher/updater. Back up an existing `Mods/BetterStorageFilter` folder before replacing its files; do not edit core mods or saves.
2. Extract the ZIP's **`BetterStorageFilter` folder into the game's `Mods` folder**. This works with either ZIP. Do not add an extra nested `Mods` or `BetterStorageFilter` folder.
3. Confirm `<game>/Mods/BetterStorageFilter/mod.json` and `<game>/Mods/BetterStorageFilter/BetterStorageFilter.dll` are siblings.
4. If using the Vortex ZIP manually, ignore the root `vortex_override_instructions.json`; it is metadata for Vortex, not a file needed in the game directory.

Launch normally through **RogueLauncher**, follow RogueTech's current safety/online rules, and open **MechBay → Storage**. All nine toggles should start ON; ordinary Reset Filters restores them. No online-play approval or integrity-check bypass is provided.

**Alt is IRTweaks' destructive bulk-scrap modifier, not a reset gesture.** Alt+Reset uses the current selected union without resetting; Alt+weight narrows that selection without toggling. Review the provider's quote before confirming; do not experiment on valued inventory merely to inspect filters.

## Verify downloads

Download `SHA256SUMS.txt` and compare the checksum for the ZIP you chose. For example, in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\BetterStorageFilter-0.2.0-vortex.zip
```

Or download both ZIPs and `release-info.json` alongside `SHA256SUMS.txt`, then run:

```sh
sha256sum --check SHA256SUMS.txt
```

Checksums detect byte changes; they are not a separate digital signature.

## Uninstall

For Vortex-managed files, disable/undeploy the mod through Vortex. For a manual installation, close the game and remove only `Mods/BetterStorageFilter`. No mod-owned campaign state or sidecar requires removal; do not delete or edit saves.

## Scope and support

The original installed 0.2.0 UI received positive user feedback. This is not an exhaustive gameplay, destructive-transaction or future-modpack compatibility guarantee. The Vortex 2.8.2 destination contract was exercised with installed code/source-map methods in a scratch sandbox, **not through a live Vortex GUI deployment**. The mod DLL is unchanged.

Use Issues with the mod/RogueTech versions, a description or screenshot and relevant redacted log excerpts. Do not post saves, credentials, launcher settings or full private logs. Source and development history remain private; this repository contains downloads, checksums, metadata and user documentation only.
