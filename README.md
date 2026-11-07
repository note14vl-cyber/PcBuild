# Redmi PC Gaming Engine

A modular, rootless Android application foundation for monitoring device resources and managing external Windows-compatibility runtimes.

## Target device
- Android 16
- ARM64
- MediaTek Helio G99 Ultra
- Mali-G57 MC2
- 6 GB RAM

## What version 0.1 does
- Displays system RAM information.
- Samples CPU time consumed by this app process (not total device CPU utilization).
- Reads Android thermal status and, where available, thermal headroom.
- Gives conservative thermal recommendations.
- Finds launchable apps whose label/package contains Winlator, GameHub, or Mobox.
- Launches a selected compatible runtime.
- Stores a user-selected game folder URI using Android's Storage Access Framework.
- Loads a small C++ NDK library and displays native device information.

## What it does not do
- It is not a Windows emulator.
- It does not run PC Building Simulator yet.
- It does not overclock or underclock CPU/GPU.
- It does not change Mali drivers or Android thermal policies.
- Selecting a folder does not automatically import it into another runtime.

## Build on GitHub Actions
1. Create a new GitHub repository.
2. Upload all project files, preserving the folder structure.
3. Open the Actions tab.
4. Enable Actions if GitHub asks.
5. Run **Build Redmi PC Gaming Engine APK**, or push to `main`.
6. Open the successful workflow run and download artifact `Redmi-PC-Gaming-Engine-debug`.
7. Extract the APK and install it on the phone.

The workflow uses JDK 17, Gradle 8.13, Android SDK 36, NDK 27.2.12479018 and CMake 3.22.1.

## Important
This is a development/debug APK. Keep Android system thermal protections enabled. The monitor reports only data exposed by Android to an ordinary app.
