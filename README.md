# BatToExeAutoConverter

Automated project for portable deployment, BAT-to-EXE packaging, ISO generation, and USB/virtual environment preparation.

## Overview

This repository provides scripts and patterns for:
- copying project files into an app root
- preparing a portable package
- building Windows `.exe` launchers
- creating ISO distributions for USB or virtual environments
- generating a structure ready for GitHub releases or local deployment

## Repository layout

```text
BatToExeAutoConverter/
├── README.md
├── requirements.txt
├── scripts/
│   ├── portable_packager.py
│   ├── build_exe.py
│   └── create_iso.py
├── examples/
│   └── sample_batch.bat
├── .github/
│   └── workflows/
│       └── release.yml
└── dist/
    └── generated_output/
```

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python scripts/portable_packager.py --source ./examples --output ./dist/portable_app --app-name DemoPortable --copy-root --build-exe --usb --virtual
```

## Notes

- `BAT` to `EXE` conversion is handled via a portable packaging workflow.
- `APK` generation would require Android tooling and is outside the scope of the base Windows portable package.
- This project is designed for GitHub-hosted automation and portable deployment tasks.

## License

MIT
