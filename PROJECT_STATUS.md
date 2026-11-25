# Project status

- Repository initialized.
- Prepared source snapshot: 13/13 host C++ tests passed.
- Android APK build: not verified in this environment.
- Retail Fallout: New Vegas boot: not verified.
- D3D9-to-Vulkan: incomplete; currently a major implementation milestone.
- APK reference 1.3.2 contains a large ARM64 native library named `libfnv.so`; the new project builds a separate `libfnv3.so`. They must not be swapped blindly.

## Next engineering milestones

1. Verify the Android CI build with the actual Android SDK/NDK runner.
2. Audit the PE loader and Win32/COM API coverage against the retail executable.
3. Implement the D3D9 device/resource/swapchain path on Vulkan.
4. Add shader translation and resource lifetime tests.
5. Test on real Snapdragon/Turnip hardware with logs and reproducible game data.
6. Validate input, audio, suspend/resume, and long-session stability.
