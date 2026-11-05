# Heronite for Scoop

[![Tests](https://github.com/RafaelGoulartB/scoop-heronite/actions/workflows/ci.yml/badge.svg)](https://github.com/RafaelGoulartB/scoop-heronite/actions/workflows/ci.yml) [![Excavator](https://github.com/RafaelGoulartB/scoop-heronite/actions/workflows/excavator.yml/badge.svg)](https://github.com/RafaelGoulartB/scoop-heronite/actions/workflows/excavator.yml)

The [Scoop](https://scoop.sh) bucket of [Heronite](https://heronite.app):
every game you own, on Linux and Windows, in one fast native launcher.

## Install

```powershell
scoop bucket add heronite https://github.com/RafaelGoulartB/scoop-heronite
scoop install heronite/heronite
```

## Update

```powershell
scoop update            # refreshes the buckets
scoop update heronite
```

Close Heronite, including from the tray, before updating: Scoop does not
replace a program that is still running. Heronite tells you when a new
version is out, and Scoop installs it.

Your library and settings are in `%APPDATA%\heronite` and
`%LOCALAPPDATA%\heronite`. They stay through updates and when you uninstall.

## How this bucket works

[`bucket/heronite.json`](bucket/heronite.json) installs the portable zip of
each [release](https://github.com/RafaelGoulartB/Heronite/releases). Its
source, and what each part does, is in Heronite's repository:
[`packaging/scoop`](https://github.com/RafaelGoulartB/Heronite/tree/main/packaging/scoop).
The Excavator workflow checks for new releases every 4 hours and updates the
manifest, with the SHA-256 taken from the release's `SHA256SUMS`.

Bugs in Heronite go to its
[issues](https://github.com/RafaelGoulartB/Heronite/issues); problems with
installing it through Scoop can go here.
