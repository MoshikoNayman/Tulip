# Tulip Planner

A desktop IP planning and network intelligence tool for IPv4 and IPv6: subnet
calculation, CIDR aggregation, route summarization, allocation planning, and
NAT64 translation. Everything runs locally, with no external services.

By Moshiko Nayman.

Proprietary software. All rights reserved.

---

## Download 26.2R1-S1

| Platform | File |
|----------|------|
| macOS (Apple Silicon) | [Tulip.Planner_26.2R1-S1_aarch64.dmg](https://github.com/MoshikoNayman/Tulip/releases/download/26.2R1-S1/Tulip.Planner_26.2R1-S1_aarch64.dmg) |
| Windows (x64) | [Tulip Planner_26.2R1-S1_x64-setup.exe](https://github.com/MoshikoNayman/Tulip/releases/download/26.2R1-S1/Tulip%20Planner_26.2R1-S1_x64-setup.exe) |
| Linux (AppImage) | [Tulip.Planner_26.2R1-S1_amd64.AppImage](https://github.com/MoshikoNayman/Tulip/releases/download/26.2R1-S1/Tulip.Planner_26.2R1-S1_amd64.AppImage) |
| Linux (deb) | [Tulip.Planner_26.2R1-S1_amd64.deb](https://github.com/MoshikoNayman/Tulip/releases/download/26.2R1-S1/Tulip.Planner_26.2R1-S1_amd64.deb) |

All builds are also listed on the [Releases](https://github.com/MoshikoNayman/Tulip/releases) page.

---

## What Is Tulip

Tulip is a desktop networking utility for working with IPv4 and IPv6 prefixes. It
is built for planning address space, checking subnet boundaries, summarizing
routes, and modeling allocation usage, without mixing that logic with external
services. All calculation happens on your machine.

## Features

- **Subnet calculator** — IPv4 and IPv6 analysis from an address and prefix length:
  network and broadcast addresses, subnet mask, usable host range, total and usable
  counts, and a binary prefix view.
- **Subnet planning** — CIDR, FLSM (fixed-length) and VLSM (variable-length)
  workflows for carving a parent prefix into child subnets.
- **Route aggregation** — deterministic binary sibling-prefix merging (RFC 4632)
  that never summarizes beyond the prefixes you provide.
- **Allocation tracking** — utilization and fragmentation visibility for a base
  network and its allocations.
- **NAT64** — RFC 6052 IPv4-embedded-IPv6 translation helpers.
- **Workspaces** — JSON import/export and CSV export of results.
- **Themes** — selectable presentation themes.

## Installing

### macOS

1. Open the `.dmg` and drag **Tulip Planner** into Applications.
2. This build is not yet notarized, so Gatekeeper may warn on first launch.
   Right-click the app and choose **Open**, or clear the quarantine flag:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/Tulip Planner.app"
   ```

### Windows

Run the `_x64-setup.exe` installer. SmartScreen may prompt because the build is
unsigned; choose **More info → Run anyway**.

### Linux

- **AppImage:** `chmod +x Tulip.Planner_*_amd64.AppImage`, then run it.
- **deb:** `sudo apt install ./Tulip.Planner_*_amd64.deb`

## System Requirements

- macOS 11 or later (Apple Silicon)
- Windows 10 or 11 (x64)
- A modern x86_64 Linux distribution

## Release Status

- Current release: **26.2R1-S1** (production release)
- The `stable` designation is governed by [RELEASE_POLICY.md](RELEASE_POLICY.md).

## Source And Development

Development work is maintained in the Tulip-Dev repository:

- https://github.com/MoshikoNayman/Tulip-Dev

This repository is reserved for production releases and release downloads.

## License

Proprietary. All rights reserved. See [LICENSE](LICENSE).
