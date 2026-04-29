# Sysmac I/O Link (Release)

<p align="center">
  <img src="assets/Sysmac-IO-Link_256.png" alt="Sysmac I/O Link Logo" width="180">
</p>

This repository hosts **public Windows releases** of **Sysmac I/O Link**.

Sysmac I/O Link bridges **Factory I/O** with the **Omron Sysmac Studio Simulator** so students can practice PLC workflows **without physical hardware**.

## Download

Go to **Releases** and download the latest `Sysmac-IO-Link.exe`.

Current release notes: `v1.2.0`

## Requirements

- Windows 10/11
- Factory I/O (SDK backend for Ultimate, or Modbus TCP backend)
- Omron Sysmac Studio with Simulator

## Quick Guide (GIFs)

### First-time setup

![First-time setup](assets/Gifts/first-run-setup.gif)

Use the full Sysmac global variables export from `Tools -> Export Global Variables -> CX-Designer`. The bridge needs datatype information for mapped variables.

### Create and save mappings

![Create and save mappings](assets/Gifts/mapping-save.gif)

### Test connections and start bridge

![Test connections and start bridge](assets/Gifts/test-and-start-bridge.gif)

## What's new in v1.2.0

- Added friendlier validation and runtime messages instead of Python traceback pop-ups.
- Bridge start is blocked when mappings, globals, addresses, backend settings, or datatypes are invalid.
- Bridge failures now report the failing mapping, for example `input:bit:5 -> S1`.
- Sysmac globals must include datatype information for mapped variables.
- Packaged builds suppress the PyInstaller traceback dialog by default.

## Troubleshooting

### Validation message appears before starting

Fix each listed item, then press `Start Bridge` again. Common causes are missing Sysmac variables, duplicate mappings, invalid addresses, unsupported Modbus types, or globals pasted without datatypes.

### Bridge stopped because an issue was detected

Read the last `[bridge]` line in the app log. It should identify the mapping or setting that failed.

### Sysmac variable has no datatype

Open `Update` beside Globals and paste the full Sysmac export table. A plain variable-name list is not enough for mapped variables.

## License

PolyForm Noncommercial 1.0.0 (see `LICENSE`).

## Third-party licenses

- Factory I/O SDK: Microsoft Public License (Ms-PL). See `LICENSES/FactoryIO-SDK-LICENSE.txt`.

[//]: # (This is a binary-only distribution.)
[//]: # (For source code, issues, and documentation, see:)
[//]: # (https://github.com/JoaquinDillen/sysmack-io-link)
