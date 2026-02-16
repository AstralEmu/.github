<p align="center">
  <img src="./banner-astralemu.svg" alt="AstralEmu Banner" width="100%"/>
</p>

<p align="center">
  <strong>A Linux distribution purpose-built for emulation.</strong><br/>
  <em>Minimal. Optimized. Ready to play.</em>
</p>

<p align="center">
  <a href="https://astralemu.github.io">📖 Documentation</a> •
  <a href="https://github.com/orgs/AstralEmu/discussions">💬 Community</a> •
  <a href="https://github.com/AstralEmu/astralemu">⭐ Main Repo</a>
</p>

---

## What is AstralEmu?

AstralEmu is a Linux distribution designed from the ground up for emulation on embedded and desktop hardware. It ships a minimal base system, a curated set of emulators rebuilt daily with performance optimizations, and a dynamic performance manager that tunes your hardware per-emulator.

Built on top of **Ubuntu**, **Debian**, **Arch Linux**, and **Universal Blue**, AstralEmu delivers multiple image variants tailored to your device and your needs.

## Key Features

🔧 **Dynamic Image Builder** — A workflow-based build system that handles service configuration, source images, export formats, filesystem shrinking, and multi-architecture builds. Images are rebuilt automatically every 24 hours.

📦 **Custom Package Repositories** — APT, DNF, and Pacman repos with daily rebuilds of every standalone emulator and RetroArch core. Each package is compiled with `LTO=thin` and `jemalloc` for maximum performance, targeting the exact CPU architecture of your device.

⚡ **Per-Emulator Performance Tuning** — A custom package per hardware target dynamically manages CPU/GPU/RAM governors, overclocking, underclocking, CPU pinning, and power-aware safety limits — all automatically, per emulator or service.

🖥️ **EmulationStation DE Frontend** — A custom-themed EmulationStation Desktop Edition as the main interface, with optional services like XFCE, Plasma Mobile, Kodi, and Waydroid. Only one service runs at a time — when a secondary service launches, ES-DE stops; when it exits, ES-DE restarts.

🔄 **Atomic Updates** — Universal Blue's native image-based update method, replicated across other base distros for a consistent, safe upgrade path everywhere.

## Repositories

| Repository | Description |
|---|---|
| [**astralemu**](https://github.com/AstralEmu/astralemu) | Main distribution — image builder, system configs, and integration |
| [**astralemu-packages**](https://github.com/AstralEmu/astralemu-packages) | APT / DNF / Pacman repos with optimized emulator builds |
| [**astralemu.github.io**](https://github.com/AstralEmu/astralemu.github.io) | Documentation & showcase (Starlight on GitHub Pages) |

## Supported Base Systems

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu"/>
  <img src="https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white" alt="Debian"/>
  <img src="https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=archlinux&logoColor=white" alt="Arch Linux"/>
  <img src="https://img.shields.io/badge/Universal_Blue-1a1a4e?style=for-the-badge&logo=fedora&logoColor=white" alt="Universal Blue"/>
</p>

---

<p align="center">
  <sub>Made with ⭐ by the AstralEmu community</sub>
</p>
