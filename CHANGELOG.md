# momentic-mobile

## 0.0.16

### Patch Changes

- 0f5ba29: Do not fallback to cloud AI agent configurations if local ones are not provided.

## 0.0.15

### Patch Changes

- e3ad980: Support merging caches back into main using the Gitlab API

## 0.0.14

### Patch Changes

- 85f5aa6: Merge caches back into main when a branch is merged on github
- d929b02: Fix bug causing caches to not be stored on main

## 0.0.13

### Patch Changes

- 2787516: Added a configuration option for android emulator region
- 2787516: Fixed a bug where the autoGrantPermissions setting was not being respected during test runs

## 0.0.12

### Patch Changes

- b861ea9: Fix asset uploading to emulator platform.

## 0.0.11

### Patch Changes

- 913e30d: Fix relative pathing for getting tests in the app

## 0.0.10

### Patch Changes

- 185aabf: Add support for us-west1 region (automatic routing based on client IP). Fix cases where unhandled promise rejections would crash the desktop app.
- 9f1159f: Filter out non-applicable test types from local apps

## 0.0.9

### Patch Changes

- af31c5a: Fix unhandled JSON circular dependency error on execute events.

## 0.0.8

### Patch Changes

- 2844c51: Add support for using environments when running mobile tests.
- 464c13d: automatically terminate editor sessions that have been idle for too long

## 0.0.7

### Patch Changes

- d817422: Opening an app no longer fails when a permission check appears.
- e3518a7: Add JavaScript step support
- 7e5e667: Change Momentic remote logger provider
- d817422: Added the ability to auto grant all permissions to the APK under test.

## 0.0.6

### Patch Changes

- 4f421d5: Add support for folders to the local app

## 0.0.5

### Patch Changes

- 23c1b92: Add validation for channel name (all lowercase is enforced now)
- b398d6f: Escape unicode characters in cache headers

## 0.0.4

### Patch Changes

- 949f37b: Fix log line for executing step count

## 0.0.3

### Patch Changes

- ac1a6fa: Drag and drop no longer duplicates steps
- 74051fb: Add JDK setup checks and improve caching performance.

## 0.0.2

### Patch Changes

- c038cc7: Automatically open the local app when running the `app` command.
