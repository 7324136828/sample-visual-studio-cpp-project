# Sample Visual Studio C++ Project

A small C++17 Windows desktop application with Debug and Release x64 configurations.
It uses the Win32 API and requires no additional libraries beyond the Windows SDK.

## Requirements

Visual Studio 2026 or its Build Tools, with the C++ desktop build tools (v145)
and a Windows 10/11 SDK installed.

## Build and run in Visual Studio

1. Open `SampleCpp.sln`.
2. Select **Debug** or **Release**, with the **x64** platform.
3. Press **Ctrl+Shift+B** to build, then **Ctrl+F5** to run.

The program opens a resizable window titled `Sample C++ Window`, with
`Hello from Visual Studio C++!` centered inside. Close the window to exit.

## Build and run from the command line

In a Visual Studio Developer PowerShell, from this folder:

```powershell
msbuild .\SampleCpp.sln /p:Configuration=Debug /p:Platform=x64
.\build\x64\Debug\SampleCpp.exe
```

Use `Configuration=Release` to build the Release configuration; its executable
is at `build\x64\Release\SampleCpp.exe`.

Edit `src/main.cpp` to change the program. Generated build files are kept under
`build/` and ignored by Git. To use Visual Studio 2022, retarget the project to
the installed v143 toolset in **Project Properties > General > Platform Toolset**.
