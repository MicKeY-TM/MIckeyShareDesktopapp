# MicKeYShare

**Your Local Files. Shared Beautifully.**

MicKeYShare is a lightweight, portable Windows desktop and local-network web file-sharing application. Select a folder on your PC, click **START SHARING**, and scan the QR code or open the LAN URL from any phone, tablet, or computer on the same Wi-Fi/LAN.

## Documentation

- **End Users:** Read [USER_GUIDE.md](USER_GUIDE.md) for easy download instructions and step-by-step usage on Windows and mobile devices.
- **Developers & Maintainers:** Read [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md) for the full architecture, security invariants, REST API contract, and upgrade/build workflow.

## Key Features

- **Portable Single-File Desktop App (`MicKeYShare.exe`)**: No installer, no Python/Node.js runtime required, no registry edits, works completely offline.
- **Simple Start / Stop Controls**: Automatically detects your active LAN IPv4 address, picks an available dynamic TCP port, generates a QR code, and revokes all active client sessions and releases the port immediately when you click **STOP SHARING**.
- **Access Modes**: Default **Download Only** mode or optional **Allow Uploads** mode with drag-and-drop, multi-file & folder uploads, live progress, cancellation, and safe conflict handling (never silently overwrites existing files).
- **Modern Responsive Web File Manager**:
  - Light & Dark themes
  - Three display modes: **Grid View**, **List View**, and **Large Icon View**
  - Category filters: All Files, Images, Videos, Audio, Documents, Archives
  - Debounced search, breadcrumbs, Back / Parent / Home navigation, and 7 sort orders
  - Multi-select files and folders with floating toolbar and streaming ZIP archive downloads
  - Rich previews: Image zoom + prev/next navigation, Video & Audio with HTTP Range seeking, PDF, and escaped Text/Code viewer
- **Security Controls**: Root folder confinement, traversal & symlink/junction escape prevention, `C:\` root block, optional PBKDF2-protected PIN lock, and epoch-bound session tokens.

## Quick Start for Developers

```powershell
# 1. Create virtual environment and install dependencies
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt

# 2. Run automated test suite
.\.venv\Scripts\python.exe -m pytest -v

# 3. Run desktop app from source
.\.venv\Scripts\python.exe main.py

# 4. Build standalone portable MicKeYShare.exe (< 50 MB)
.\.venv\Scripts\python.exe build_exe.py
```
