# SDL3 GPU + C++23 - IMGUI example
---
Using IMGUI with SDL3 gpu and C++23

### CMake commands for configuring and building
VSCode will run these automatically.
- On Windows
```shell
  # Configure Project
  cmake --preset windows-default
  # Build Project, parameter order matters
  cmake --build --preset windows-debug
```
- On Linux
```shell
  # Configure Project
  cmake --preset linux-default
  # Build Project, parameter order matters
  cmake --build --preset linux-debug
```

## Uses/Dependencies
- CPM.CMake for package management
- Ninja-Build for build engine
- CMake 3.31+ with cmakepresets for configuration and build
  - There is an issue, on my machine, with CMake 4.0. It fails to configure properly.
  - CMake 4.0.1 fixed the issue with configure, seems like it was regression in CMake.
- C++ modules enabled
- Uses C++ Standard Library modules
  - MSVC (Windows only)
  - Clang (Linux with libc++ only)
- Focuses on SDL3 GPU
- HLSL for all shaders, compile to SPIRV for Vulkan and DXIL for Direct3D

## References
- <https://github.com/ocornut/imgui/blob/master/examples/example_sdl3_sdlgpu3/main.cpp>