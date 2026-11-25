# Architecture roadmap

## Stage 1 — foundation
- Android application shell and native bridge.
- ARM64 target.
- Initial PE loading and compatibility scaffolding.
- Input and audio abstraction prototypes.
- Host-side tests.

## Stage 2 — Win32 and system API compatibility
- Expand imports and API coverage required by the retail executable.
- Complete thread, synchronization, TLS, registry, filesystem, and COM behavior.
- Validate calling conventions, structure layouts, and error semantics on ARM64.

## Stage 3 — graphics
- Implement D3D9 interfaces and device lifecycle.
- Map D3D9 resources, render states, shaders, and presentation to Vulkan.
- Implement shader model 3 translation to SPIR-V.
- Validate depth/stencil, render targets, textures, buffers, and swapchain behavior.
- Do not mark this stage complete until actual retail-game frames render on device.

## Stage 4 — on-device game validation
- Boot retail game data on supported ARM64 devices.
- Validate menus, gameplay, saves, audio, input, and suspend/resume.
- Profile CPU/GPU/RAM and fix crashes and rendering defects.

## Exit criteria
A passing host test suite is not proof of Android build success or game compatibility. A milestone is complete only with reproducible tests and device evidence.
