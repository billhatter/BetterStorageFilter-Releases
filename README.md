# Better Storage Filter — downloads

Binary releases and supporting documentation for **Better Storage Filter**, a RogueTech-required ModTek mod for **HBS BATTLETECH → MechBay → Storage**. This is not the post-mission salvage screen and is not a vanilla-game mod.

This repository contains **downloads, checksums, release metadata and user documentation only**. Project source and development history are not published here.

## Download 0.2.0 (beta)

- [Mod ZIP: BetterStorageFilter-0.2.0-mvp.zip](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/BetterStorageFilter-0.2.0-mvp.zip)
- [SHA-256 checksums](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/SHA256SUMS.txt)
- [Release metadata and individual payload hashes](https://github.com/billhatter/BetterStorageFilter-Releases/releases/download/v0.2.0/release-info.json)
- [Release page](https://github.com/billhatter/BetterStorageFilter-Releases/releases/tag/v0.2.0)

**Download the named mod ZIP above.** GitHub's automatic “Source code” ZIP/tar.gz files contain this repository's documentation/checksums, not the mod installer or project source.

## Features

- Five independent type toggles: Mechs, Vehicles (ground), Battle Armor, VTOLs and ProtoMechs.
- Four independent weight toggles: Light, Medium, Heavy and Assault.
- Choices combine within each row; the type and weight rows intersect.
- All nine toggles start ON. **Reset Filters** enables them all.
- Turning every toggle OFF in either row shows no matches; OFF buttons remain clickable.
- Complete stored units and parts share the filters. Selections remain in runtime memory, not campaign-save data.
- Existing CustomFilters virtualization and IRTweaks provider-owned bulk-scrap workflow are retained.

## Requirements and compatibility

Requires ModTek and the RogueTech stack providing the exact manifest dependencies **RogueTech Core**, **CustomUnits**, **CustomFilters** and **IRTweaks**. Game/dependency DLLs are not bundled. RogueTech updates can change integration contracts; compatibility with every future pack update is not implied.

This is a **beta** distribution. The build passed its recorded automated checks, and the installed UI received positive user feedback. This is not certification of every live-game combination or destructive transaction. No RogueTech online approval is claimed. Use only configurations permitted by the current RogueTech launcher; do not bypass online integrity checks or change launch safety to force loading.

## Verify the download

The ZIP's SHA-256 is:

```text
c305b726174ad5ae49bb3404fdc1e6b00f3346b89f57d90fb018e55a43920614
```

On Windows, compare the output of PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\BetterStorageFilter-0.2.0-mvp.zip
```

Or download all three assets into one directory and run:

```sh
sha256sum --check SHA256SUMS.txt
```

Checksums detect byte changes; they are not a separate digital signature.

## Installation / upgrade

1. Close BATTLETECH and the RogueTech launcher/updater before changing files.
2. Back up any existing `Mods/BetterStorageFilter` folder before upgrading. Do not alter core mods or saves.
3. Verify and extract the mod ZIP into the game's `Mods` directory. The resulting siblings must include `Mods/BetterStorageFilter/mod.json` and `Mods/BetterStorageFilter/BetterStorageFilter.dll`.
4. Launch through your normal permitted RogueTech setup, then open **MechBay → Storage**. All nine toggles should start ON; ordinary Reset Filters restores them.

**Alt is IRTweaks' destructive bulk-scrap modifier, not another reset gesture.** Alt+Reset uses the current selected union without resetting it; Alt+weight narrows that selection to the clicked weight without toggling. Review the provider's quote before confirming. Do not test destructive shortcuts on valued inventory just to inspect the filters.

To uninstall, close the game and remove only this mod's folder. No mod-owned campaign state or sidecar needs removal; do not delete or edit saves. RogueTech updates may replace or remove local mods.

## Support

Use this repository's Issues with the mod version, RogueTech version, a description/screenshot of the Storage problem and relevant redacted log excerpts. Do not post saves, credentials, launcher settings or full private logs.
