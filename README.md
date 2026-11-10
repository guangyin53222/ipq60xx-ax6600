# ipq60xx-ax6600

Custom OpenWrt build configuration and package overlay for IPQ60XX/AX6600-based routers, with a preconfigured firmware profile and a local `athena-led` package set for the JDCloud AX6600 LED controller.

This repository is designed to be used as a source overlay for an OpenWrt/ImmortalWrt build. It contains:

- target configuration files for specific device variants
- package injection scripts for custom feeds and apps
- filesystem overlays under `files/`
- local package definitions for `athena-led` and `luci-app-athena-led`
- GitHub Actions workflows that automate full firmware builds

## Overview

The project targets Qualcomm IPQ60XX platforms, especially AX6600-class devices. It assembles a custom OpenWrt firmware by:

1. cloning a base OpenWrt/ImmortalWrt source tree
2. injecting local files and packages into the build tree
3. applying custom settings and package lists
4. compiling a release image via GitHub Actions

This repo is especially useful for users who want a customized firmware with:

- selected OpenWrt packages and themes
- network and system tweaks
- `athena-led` support
- custom LuCI integration
- reproducible cloud builds

## Repository structure

```text
.
├── .github/
│   ├── scripts/
│   └── workflows/
├── Config/
│   ├── GENERAL.txt
│   ├── IPQ60XX-WIFI-YES.txt
│   └── TEST.txt
├── Scripts/
│   ├── Handles.sh
│   ├── Packages.sh
│   └── Settings.sh
├── files/
│   └── etc/
├── package/
│   ├── athena-led/
│   └── luci-app-athena-led/
├── LICENSE
├── README.md
└── ...
