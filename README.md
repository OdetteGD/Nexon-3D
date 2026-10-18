# Nexon-3D

Nexon-3D is a native C++ mobile 3D engine and editor for Android, built around a Vulkan renderer and a desktop-like editor layout. The repository includes:

- Android app shell and native window bridge
- Vulkan initialization for Android surfaces
- C++ scene/editor engine foundation
- hierarchy-panel UI layout for an editor-inspired mobile workspace
- GitHub Actions workflow to build a debug APK

This is a production-grade foundation, not a complete AAA engine. It is structured so the engine, renderer, and editor can evolve into a full real-time editor/editor stack.

## Build

Requirements:
- Android SDK + NDK installed
- JDK 11+
- Android platform 31 or newer

Build with Gradle:

```
gradle assembleDebug
```

Or if you use the Android SDK command line tools:

```
./gradlew assembleDebug
```

## Run

Install the APK from app/build/outputs/apk/debug/ on a connected Android device:

```
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

## Project Structure

- `app/` — Android application
- `engine/` — engine runtime and renderer
- `editor/` — editor hierarchy and scene components
- `.github/workflows/android-build.yml` — CI APK build

## Notes

This foundation includes actual native Vulkan initialization and an Android UI skeleton. It is intentionally designed to be expanded with a real scene graph, input system, ECS, material pipeline, and editor tooling.
