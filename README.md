# Scoop bucket for Ferryfile

[![Tests](https://github.com/ahm3d-karim/scoop-ferryfile/actions/workflows/ci.yml/badge.svg)](https://github.com/ahm3d-karim/scoop-ferryfile/actions/workflows/ci.yml) [![Excavator](https://github.com/ahm3d-karim/scoop-ferryfile/actions/workflows/excavator.yml/badge.svg)](https://github.com/ahm3d-karim/scoop-ferryfile/actions/workflows/excavator.yml)

[Scoop](https://scoop.sh) bucket for [Ferryfile](https://github.com/ahm3d-karim/ferryfile),
an offline, drag-and-drop file converter for Windows.

## Install

```pwsh
scoop bucket add ferryfile https://github.com/ahm3d-karim/scoop-ferryfile
scoop install ferryfile/ferryfile
```

Scoop installs the portable build (Ferryfile plus its bundled FFmpeg, pandoc
and PDFium) and adds a **Ferryfile** Start menu shortcut. Ferryfile runs in the
system tray; drag a file from Explorer to open its drawer.

Update with `scoop update ferryfile`, remove with `scoop uninstall ferryfile`.

## How this bucket updates

`bucket/ferryfile.json` has `checkver` and `autoupdate` rules. The
[Excavator](.github/workflows/excavator.yml) workflow runs every 4 hours, finds
new Ferryfile releases on GitHub, reads their published `.sha256` checksums and
commits the updated manifest.
