<p align="center">
  <img src="https://github.com/AstralEmu/.github/raw/refs/heads/main/profile/banner-astralemu.svg" alt="AstralEmu" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/focus-console%20modding%20%26%20emulation-f2d974?style=flat-square" alt="Focus"/>
  <img src="https://img.shields.io/badge/platform-Nintendo%20Switch%20|%20Atmosphere%20|%20Ryujinx-1a1a4e?style=flat-square" alt="Platform"/>
  <img src="https://img.shields.io/badge/license-GPL%20|%20MIT-blue?style=flat-square" alt="License"/>
</p>

## About

**AstralEmu** is an open-source organization focused on **console modding and emulation**. We build tools that make custom firmware setups and emulator features easier to install, easier to keep up to date, and closer to plug-and-play.

Our work currently centers on the Nintendo Switch ecosystem: Atmosphere sysmodules, automated homebrew pack builds, and local-wireless multiplayer for the Ryujinx emulator.

## Projects

| Project | Description | Language | License |
|---|---|---|---|
| [**RyuLdnNX**](https://github.com/AstralEmu/RyuLdnNX) | Atmosphere sysmodule that bridges Switch LDN multiplayer to the Ryujinx LDN protocol. Aims to replace `ldn_mitm` and `lan-play` with a single, zero-config module. | C++ | GPL-2.0 |
| [**AstralPack**](https://github.com/AstralEmu/AstralPack) | Automated builder for Switch CFW packs. Pulls the latest releases of each component and assembles a ready-to-extract zip. | Python | GPL-3.0 |
| [**LdnServer**](https://github.com/AstralEmu/LdnServer) | Server that manages LDN game sessions for pseudo-online multiplayer in Ryujinx. Fork of [Ryubing/LdnServer](https://github.com/Ryubing/LdnServer). | C# | MIT |
| [**LdnWebsite**](https://github.com/AstralEmu/LdnWebsite) | Web frontend for the LDN server. Fork of [Ryubing/LdnWebsite](https://github.com/Ryubing/LdnWebsite). | TypeScript | MIT |

### RyuLdnNX

Play LDN-capable Switch games online through the Ryujinx LDN network, straight from real hardware.

- Plug-and-play install: extract to the SD card, reboot, play
- Intercepts `ldn:u` and `bsd:u` and tunnels LDN traffic to a Ryujinx LDN server
- Tesla overlay for live status and configuration
- Optional direct peer-to-peer connections via UPnP

> [!NOTE]
> RyuLdnNX is a work in progress. Use a private RyuLDN server when testing rather than the official Ryujinx servers.

Documentation: [astralemu.github.io/RyuLdnNX](https://astralemu.github.io/RyuLdnNX/)

### AstralPack

A pack builder driven by a single `components.json` manifest. Each build:

1. Resolves the latest GitHub release of every listed component
2. Applies per-component processing steps (unzip to root, copy, rename, delete)
3. Adds the HATS installer payload and writes its config
4. Outputs a dated, hashed zip along with a manifest and a changelog against the previous build

Components include Atmosphere, Hekate, sigpatches, Tesla overlays (Ultrahand, sys-clk, emuiibo, Status Monitor), homebrew apps (Sphaira, JKSV, AIO-Switch-Updater) and payloads (TegraExplorer, Lockpick_RCM).

## Contributing

Contributions are welcome on every project. Before opening an issue or pull request, please read:

- [Contributing guidelines](https://github.com/AstralEmu/.github/blob/main/CONTRIBUTING.md)
- [Code of Conduct](https://github.com/AstralEmu/.github/blob/main/CODE_OF_CONDUCT.md)
- [Security policy](https://github.com/AstralEmu/.github/blob/main/SECURITY.md)

Some projects require commits to be signed off (DCO), so check each repository's own guide.

## Disclaimer

AstralEmu does not distribute copyrighted games, firmware, or encryption keys, and does not endorse piracy. Our tools are intended for use with legally obtained software and hardware you own. We are not affiliated with Nintendo.
