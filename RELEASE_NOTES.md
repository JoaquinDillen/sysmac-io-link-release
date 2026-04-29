## Sysmac I/O Link v1.2.0

### Highlights
- Added friendly app-level error handling so common student mistakes show clear messages instead of Python traceback pop-ups.
- Added stronger validation before bridge start for mappings, globals, backend settings, addresses, duplicate mappings, and Sysmac datatypes.
- Added clearer bridge runtime messages that identify the failing mapping, such as `input:bit:5 -> S1`.
- Added safer handling for invalid or damaged configuration JSON files.
- Added validation that mapped Sysmac variables must come from a full globals export with datatype information.
- Packaged builds now suppress PyInstaller's windowed traceback dialog by default.

### Important globals change
- Use `Tools -> Export Global Variables -> CX-Designer` in Sysmac Studio.
- Paste the full exported table into the app's Globals setup.
- Plain variable-name lists are no longer enough for mapped variables because the bridge needs datatypes to pack values correctly.

### Factory backend behavior
- `SDK`: uses Factory I/O SDK memory map (Ultimate workflow).
- `Modbus TCP`: uses Factory I/O Modbus TCP addresses from the Factory I/O driver mapping.
- Mapping `address` is interpreted by the selected backend.

### Requirements
- Windows 10/11
- Factory I/O (SDK backend for Ultimate, or Modbus TCP backend)
- Omron Sysmac Studio with Simulator

### Installation
- Download `Sysmac-IO-Link.exe` from Releases.
- Run the application; no installer is required.

### SHA256
- Publish the SHA256 after the final `Sysmac-IO-Link.exe` is built and uploaded.

### Notes
- Binary-only public release repository.
- Commercial use is not permitted (PolyForm Noncommercial).
