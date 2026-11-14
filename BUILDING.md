# Building Alite with Gradle

Initial migration from the retired Ant/ADT build to Android Gradle Plugin 8.6.1.

## Requirements
- JDK 17
- Gradle 8.7
- Android SDK Platform 35

## Build
From the repository root, run:

    gradle :app:assembleDebug

The APK is written to app/build/outputs/apk/debug/app-debug.apk.

## Notes
- Legacy sources remain in src/, res/, and assets/.
- The in-tree AliteConfig.java sets HAS_EXTENSION_APK=false. The old Ant-only
  config-generation target is not used by Gradle.
- SDK levels are configured in app/build.gradle.
- Runtime behavior on Android 15, including storage, alarms, and notifications,
  still requires device testing.
