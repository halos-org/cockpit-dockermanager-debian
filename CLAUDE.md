# Cockpit Docker Manager - Debian Packaging

Debian packaging repository for cockpit-dockermanager.

## Purpose

This repository contains only Debian packaging files for building .deb packages of cockpit-dockermanager. The upstream source is maintained separately at https://github.com/chrisjbawden/cockpit-dockermanager.

## Structure

- `debian/` - Standard Debian packaging directory
  - `control` - Package metadata and dependencies
  - `rules` - Build instructions (uses dh with minimal overrides)
  - `changelog` - Version history in Debian format
  - `copyright` - License information (machine-readable format)
  - `install` - File installation mappings
  - `compat` - Debhelper compatibility level (13)
  - `source/format` - Source package format (3.0 quilt)

## Building

The build process expects the upstream source to be cloned as `cockpit-dockermanager/` in this directory:

```bash
git clone https://github.com/chrisjbawden/cockpit-dockermanager.git
dpkg-buildpackage -us -uc -b
```

## Package Details

- Package name: cockpit-dockermanager
- Architecture: all (pure JavaScript/HTML/CSS)
- Dependencies: cockpit (>= 200)
- Recommends: docker.io | docker-ce
- Installation path: /usr/share/cockpit/dockermanager/

## Versioning

Follow upstream versions. Use Debian revision -1 for initial packaging of each upstream version (e.g., 1.0.7-1).

## Maintainer

Matti Airas <matti.airas@hatlabs.fi>
