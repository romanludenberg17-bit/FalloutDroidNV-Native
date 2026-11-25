# FalloutDroidNV-Native

A native Android porting project for Fallout: New Vegas.

## Current state

This repository is being initialized from the separately prepared source archive. The current prototype contains Android/Kotlin UI scaffolding, a C++ native layer, PE/Win32 compatibility scaffolding, audio abstractions, and a Vulkan renderer skeleton.

**Important:** this is not yet a playable port. Retail-game boot and rendering are not verified. The D3D9-to-Vulkan implementation and broad Win32/COM compatibility remain major blockers.

## Build

The Android release workflow is in `.github/workflows/build-release.yml`. It requires Android SDK/NDK setup supplied by GitHub Actions. Build success does not imply that the retail game can boot.

## Tests

The host-side C++ test suite is under `tests/`. The prepared snapshot passed 13/13 host tests. These tests do not validate Android packaging, GPU rendering, or in-game compatibility.

## Project rules

- Target Android ARM64 first.
- Keep the native renderer and compatibility layers explicit; do not claim compatibility based on stubs.
- Do not replace the APK reference's `libfnv.so` with the new project's `libfnv3.so`; they are different binaries and not interchangeable.
- Use legally obtained game data supplied by the user; no game assets are included here.

See [PROJECT_STATUS.md](PROJECT_STATUS.md) and [ARCHITECTURE_ROADMAP.md](ARCHITECTURE_ROADMAP.md).
