# Pop n' Controller Hotcade.uy

Small Windows tool that bridges an Arduino Nano Pop'n Music controller to keyboard input, with a compact GUI and automatic COM detection.

Built for event setups and plug-and-play use.

## Features
- Auto-detect Arduino serial port (CH340 / USB Serial / Arduino)
- Debounced button input (press/release)
- Small GUI with status + log
- Custom branding (logo + window title)
- Packable as a portable `.exe` via PyInstaller

## How it works
Arduino Nano sends button events over Serial (`D,<index>` / `U,<index>`).  
The PC app reads those events and triggers keyboard presses/releases.

## Requirements (dev)
- Python 3.10+ (works on Windows)
- Packages: `pyserial`, `pynput`, `pillow` (if logo scaling is enabled)

Install:
```bash
pip install -r requirements.txt
