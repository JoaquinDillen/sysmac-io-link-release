## Sysmac I/O Link v1.1.0

### Highlights
- Added explicit Factory backend selection: `SDK` or `Modbus TCP`
- Removed automatic backend fallback mode
- Added backend-aware connection tests and bridge start checks
- Added Modbus type validation in mappings (prevents unsupported types)
- Added Modbus TCP PoC server script for communication testing
- Updated manuals and GIF guide with backend/addressing behavior

### Factory backend behavior
- `SDK`: uses Factory I/O SDK memory map (Ultimate workflow)
- `Modbus TCP`: uses Factory I/O Modbus TCP addresses from driver mapping
- Mapping `address` is interpreted by the selected backend

### Requirements
- Windows 10/11
- Factory I/O (SDK backend for Ultimate, or Modbus TCP backend)
- Omron Sysmac Studio with Simulator

### Installation
- Download `Sysmac-IO-Link.exe` from Releases
- Run the application (no installer required)

### SHA256
- Sysmac-IO-Link.exe: `A6192113BFA6088407AF7EAC01AE76352CDFFD00E602577F0FC4B5269E36B7E6`

### Notes
- Binary-only release
- Commercial use is not permitted (PolyForm Noncommercial)
