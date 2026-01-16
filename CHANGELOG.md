# momentic-mobile

## 0.21.2

### Patch Changes

- 1b9383e: Fix failure recovery sometimes executing on desktop app test runs
- bba2c7b: Fix a bug where caches were being saved incorrectly for failing test runs

## 0.21.1

### Patch Changes

- 71277fd: Remove unrelated logs for the list command output

## 0.21.0

### Minor Changes

- abf8fbd: Add support for overriding git metadata using environment variables

## 0.20.3

### Patch Changes

- bd8e2a1: Eliminate waiting for screenshot stability on app launch as well to reduce latency

## 0.20.2

### Patch Changes

- 04688b3: Fix mobile failure recovery not saving failure recovery details to results

## 0.20.1

### Patch Changes

- 8fd997f: Add "assets download" command to pull a previously uploaded asset from Momentic's servers
- 8fd997f: Speed improvements for running a variety of steps within webviews

## 0.20.0

### Minor Changes

- dbf1197: Failure recovery in mobile tests

## 0.19.1

### Patch Changes

- 712604f: Fix async promise rejection error when node highlights fail

## 0.19.0

### Minor Changes

- a3ea1d1: Add '--reporter' flag with support for junit for the mobile cli

## 0.18.0

### Minor Changes

- e014152: Add rotate orientation step type
- e014152: Add frame to mobile emulator

### Patch Changes

- d1a4ca2: Show mobile run failure details in the run viewer on app.momentic.ai, and log fatal errors to the console as well
- 7f73bce: Fix cache resolution bug when running tests outside of CI on main

## 0.17.0

### Minor Changes

- 132d0a1: Add label support to mobile tests, editable through repository view test details pane and supported in run group filtering

## 0.16.3

### Patch Changes

- ee96a70: Preserve test execution status and traces during background data refetches

## 0.16.2

### Patch Changes

- b5655ef: Executing an AI action inside a module no longer triggers a pull page error

## 0.16.1

### Patch Changes

- bedd1b7: Add automatic network diagnostics when using remote regions
- 06f53a6: Add quick directory output locations in mobile ADD FILE step
- 388067e: Improve cache v3 requirement generation

## 0.16.0

### Minor Changes

- 26b0199: Add list command to mobile cli and add include/exclude filters for run command

### Patch Changes

- c26b2d5: Logcat logs saved and exported for editor sessions.

## 0.15.1

### Patch Changes

- 514244c: Fix validation issue preventing filling step info with multiple fields

## 0.15.0

### Minor Changes

- 9104af2: Create a separate page for managing environments in the mobile local app.
- 9104af2: Allow configuring local AVD ID and path through the environment.

### Patch Changes

- dcdbae8: Fix a bug that caused certain caches to bust unnecessarily inside iframes
- 32457c8: Support emulators in the asia south region(beta)
- 915fb5a: Support graceful best effort reconnection for local emulators (up to 1hr)
- 80b7ce0: Mobile locator agent prompt tuning and model improvement.
- 9104af2: Default creation of new tests to 1 retry
- 9e55eec: Fix drag and drop not working in webviews

## 0.14.0

### Minor Changes

- ba87e1d: Add ability to edit name and description of tests from Repository view

### Patch Changes

- 2acc865: Surface error state when emualator disconnects

## 0.13.2

### Patch Changes

- 861a0b4: Numeric inputs no longer allow letter inputs.
- 528e9c0: Consolidate "Outputs" in step editor and fix assets column width
- 6b37353: Fix issue with drag and drop input fields being reset on blur

## 0.13.1

### Patch Changes

- c059bbd: Fix request step schema parsing errors
- 5c733be: Show APK details in the overview tab of the run viewer

## 0.13.0

### Minor Changes

- c3913d6: Upgrade models for mobile locator and mobile assertion
- c3913d6: Support memory for mobile assertions and locator calls, configurable both in momentic.config.yaml and at the test level. Defaults to ON.

### Patch Changes

- c3913d6: Support sharding when running mobile tests
- 44d0c30: Improve input for OPEN APP step by providing list of available apks

## 0.12.2

### Patch Changes

- 050800c: Detect and prevent duplicate local emulator sessions
- a33a3b1: Update momentic.config file to allow specifying repository root to display in UI

## 0.12.1

### Patch Changes

- 9fdae76: Fix issue with hanlding numerical values in DOM processing

## 0.12.0

### Minor Changes

- 3bd2528: Add toggle settings mobile step type

## 0.11.0

### Minor Changes

- ef6a5dd: Add tolerances to cache attributes and improve locator and assertion prompts

### Patch Changes

- c128c22: Fix issue with module parameters and description not saving

## 0.10.0

### Minor Changes

- 30a0179: Add reasoning section to step config pane

### Patch Changes

- 9184873: Automatically allocate more RAM for local emulators based on available machine specs
- 9184873: Add retry to appium UIAutomator2 server initialization

## 0.9.6

### Patch Changes

- d80023c: Normalize headers in request command

## 0.9.5

### Patch Changes

- 1d05bfc: Add debug logging for local AVD creation

## 0.9.4

### Patch Changes

- f0b8c4e: Add support for the drag and drop step
- 34b2281: Change ordering of keys in test files

## 0.9.3

### Patch Changes

- f0902e9: Fix issue where choosing "latest available" through the edit test options menu would incorrectly choose the literal tag **NONE**

## 0.9.2

### Patch Changes

- a52493d: Update navigation section header link styles to appear clickable

## 0.9.1

### Patch Changes

- c146c24: Improve test search performance

## 0.9.0

### Minor Changes

- be687d5: Add new Element Check step type
- 6983b6e: Add support for form-urlencoded API request bodies
- afe2df5: Show output in step config pane when running step in app

### Patch Changes

- d169573: Stop appending '.test' to every run name
- e801f0d: Fix a bug in the REQUEST step where content type was not set according to the body type chosen
- d4b4c70: Respect --regenerate-caches flag in the CLI
- d4b4c70: Fix the direction of swiping when using custom x/y coordinates
- 773a4f8: Ai Actions on mobile now how access to "swipe" and "scroll to" step types.
- d4b4c70: Make git repository metadata more consistent when running on CircleCI
- d4b4c70: Change swipe implementation in webviews to emit touch actions and drag the mouse, as opposed to scrolling the mouse
- 847ae7d: Also serialize elements with background images and no children as images in the accessibility tree
- d4b4c70: Display x/y coordinate indicator in the mobile editor

## 0.8.0

### Minor Changes

- d329656: Add uninstall app mobile step type

### Patch Changes

- 946822c: Add more checks to make sure that selectors still resolve to the same element after cache resolution

## 0.7.2

### Patch Changes

- 4d79e7e: Fix add before, add after, switching step types making the step not selectable, and switching to module
- ec02c2a: Support the new SCROLL_TO command, which scrolls to an element in native contexts
- 4d79e7e: Show AI ACTION trajectory and result

## 0.7.1

### Patch Changes

- c878f84: Always serialize labels in the web a11y tree
- c878f84: Serialize parents of momentic-ineligible elements to provide more context

## 0.7.0

### Minor Changes

- 6301fd3: Add new screen check step type

## 0.6.0

### Minor Changes

- bff59bd: Be able to run from a specified step via the editor context menu

### Patch Changes

- d636332: Record reason why caches did not resolve
- d636332: Support resolving caches with a single selector

## 0.5.0

### Minor Changes

- 1a2fe66: Support mocking android device location

## 0.4.8

### Patch Changes

- 982cef1: Fix some cases where Android 15 version would not be respected
- 09ebf4c: Change implementation for how non-input elements are cleared during TYPE steps in webviews
- c0e487f: Fix a bug where caches were being discarded despite being usable

## 0.4.7

### Patch Changes

- 033b051: Swipe % input should be a whole number

## 0.4.6

### Patch Changes

- 481d971: Fix number validation for inputs and schema validation when there are multiple fields being validated
- 00b1be0: Fix vulnerable dependencies
- 2d6e0d3: Allow users to control when to force clear content, even for elements that are not inputs or textareas

## 0.4.5

### Patch Changes

- d137b25: Fix issue where newly created modules crashed the editor

## 0.4.4

### Patch Changes

- 663c7da: Be able to configure JAVASCRIPT step's env key

## 0.4.3

### Patch Changes

- 00d1a73: New editor UI

## 0.4.2

### Patch Changes

- 86c50d3: Support Android 15 when using remote emulators
- 86c50d3: Tune swipe to only use 80% of the container size by default

## 0.4.1

### Patch Changes

- cbc6461: Add an extra layer of validation to ensure that the page doesn't change after caches are resolved

## 0.4.0

### Minor Changes

- 5c2c606: Support running Momentic Mobile against a local emulator and existing AVD. This mode can be entered by changing the Region in test options to "Local" and then configuring an AVD and optionally a path to an APK on disk.

## 0.3.1

### Patch Changes

- 61aaa3d: Use System.PullRequest.SourceBranch to infer branch for Azure devops workflows triggered by PRs

## 0.3.0

### Minor Changes

- d3f4d0f: Upgrade to latest playwright

### Patch Changes

- 9ac963d: Upgrade dependencies to address security vulnerabilities

## 0.2.3

### Patch Changes

- baf3009: Fix a bug where we weren't focusing the element before typing in webviews

## 0.2.2

### Patch Changes

- e944e96: Improvements to mobile logs table including auto-scrolling and emulator filter

## 0.2.1

### Patch Changes

- 99f3794: Add a visual indicator when caches aren't being saved in the editor

## 0.2.0

### Minor Changes

- ca32829: Add a --regenerate-caches flag to rebuild caches from scratch

### Patch Changes

- ef7f855: Respect retries configured in momentic.config.yaml
- c824bc5: Add new command to kill an app and remove it from backgrounding
- 2e211cc: Fix a date parsing bug impacting safari

## 0.1.2

### Patch Changes

- 5af3fff: Support setting retries at the test level in the test options dialog

## 0.1.1

### Patch Changes

- bfd938e: Fix bug where AI action steps did not write proper results when executed through `momentic-mobile run`
- bfd938e: Optimize the latency of taking screenshots of the emulator

## 0.1.0

### Minor Changes

- a62310c: Add AI action support to Momentic mobile

### Patch Changes

- 799c437: Fix bug causing mobile to not respect the agent config specified in the momentic.config.yaml
- b7f9758: Improve error messages when merging results fails due to validation errors

## 0.0.30

### Patch Changes

- 6b504f8: Support keypress delay for TYPE steps in the UI

## 0.0.29

### Patch Changes

- 712bf7d: Add Accessibility tab to editor view to view and download the current accessibility xml tree

## 0.0.28

### Patch Changes

- 3fc6548: Fix clear content for typing in webviews

## 0.0.27

### Patch Changes

- 3b72364: Disable service workers by default to reduce flakiness when intercepting requests and to combat an instance where Playwright can hang indefinitely on sites using service workers: https://github.com/microsoft/playwright/issues/37347.
- 71c4ec4: Visual improvements to the logcat viewer in the editor

## 0.0.26

### Patch Changes

- 59e74f6: Add better validation for the tap step inputs

## 0.0.25

### Patch Changes

- df91827: Add filtering for logcat logs
- 7654bbb: Add options for TAP (double tap, long press, relative position), TYPE (clear content), JAVASCRIPT (timeout), and AI CHECK (timeout) to the mobile editor UI

## 0.0.24

### Patch Changes

- dbe2ac7: Show logcat logs in the editor
- c51013a: Collect logcat logs from test runs
- 17d40ee: Add additional confirmation if the user initializes a Momentic configuration outside of a Git repo

## 0.0.23

### Patch Changes

- 8045d6a: Show md5 hash and correct updated time in the assets table
- 92777c9: Add file step to create files on the virtual device

## 0.0.22

### Patch Changes

- ed3b654: Flip useMomenticAccessibilityTree to disableMomenticAccessibilityTree so that the Momentic implementation is enabled by default
- 51ccafc: Add double tap option to tap step
- ed3b654: Fix bug where screenshots would not be captured for the final failing step(if there is one).
- ed3b654: Add support for swiping up/down/left/right and various options

## 0.0.21

### Patch Changes

- ed694bd: Add support for WAIT and API REQUEST steps on the backend
- 66510e7: Loosen threshold for screenshot comparisons when waiting for stability
- 66510e7: Add ability to specify relative coordinates when tapping a target
- 66510e7: Introduce "useMomenticAccessibilityTree" option in tests and at the org-level to always prefer using the momentic accessibility tree implementation for webviews, which captures far more elements

## 0.0.20

### Patch Changes

- c5a2196: fixed a bug that was preventing caches from being saved

## 0.0.19

### Patch Changes

- 72292d2: Add timeouts for all mobile driver commands
- 72292d2: Add backend support for modules
- 72292d2: Add keyboard press step type for pressing special keyboard keys
- e5e7a9f: Show navigation breadcrumbs in the test editor
- 72292d2: Add backend options for long press, key press delay, and clearing content

## 0.0.18

### Patch Changes

- 7ca8d7f: Fix nav item styling
- 28b3921: Attempt to send logs on node crashes

## 0.0.17

### Patch Changes

- 7aa0d79: Respect quarantined tests

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
