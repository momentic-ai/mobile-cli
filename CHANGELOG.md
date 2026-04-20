# momentic-mobile

## 0.77.2

### Patch Changes

- 4313b4f: Show AI Action version in run viewer

## 0.77.1

### Patch Changes

- cc4fcbd: Fix a bug where tests were not shown in the local app UI on Windows

## 0.77.0

### Minor Changes

- ce25160: Remove get intial data to instead move the step schema onto the session start tool. Updated the skill to match the new edit procedure.

### Patch Changes

- 6259dbc: Update Run Viewer UI to have resizable panels, floating step info card
- fbe5a7d: Fix video player hover CSS being hard to read

## 0.76.1

### Patch Changes

- 7c7aa07: Improve globbing performance
- 7c7aa07: Exclude dependency directories from config yaml file search
- 0acb6d7: Fix mcp bug where the project emulator defaults were being overridden when making new mcp sessions. Start session now correctly follows tool input, test, then project config precedence order.
- 57880bd: Improve iOS cache resolution
- 99e77ec: Make the daemon not connect to daemons from other cli versions.

## 0.76.0

### Minor Changes

- 923d0b7: Add a --daemon flag to the MCP to enable a background daemon to maintain sessions across separate server invocations. Note: this is not available for windows yet.

### Patch Changes

- fb04242: Reorganize editor step input elements

## 0.75.1

### Patch Changes

- b411490: Fix editor keybindings so that i and e now begin editing the default section of the selected step.
- df3138a: Exclude more directories from globbing by default
- 7b02efd: Prevent unintentional exits during test runs
- c3a6745: Fix default sizing for editor bottom panel

## 0.75.0

### Minor Changes

- 49588d5: Add AI Action v3 for Android

## 0.74.2

### Patch Changes

- 312aec5: Update iOS and Android models to be faster for AI Action
- 312aec5: Fix error that occurs during OpenAI fallbacks where reasoning summaries would cause fatal message mismatch exceptions

## 0.74.1

### Patch Changes

- 7cbb2b5: Improve auth check error messages with actionable guidance

## 0.74.0

### Minor Changes

- fff5af6: Add Android video recording support. Screen recordings are now automatically captured during Android test runs on remote emulators.
- 452974f: Support opt-in native a11y tree for iOS

### Patch Changes

- b22cce8: Convert step editor form inputs to use code mirror to handle template string syntax highlighting
- a41dea2: Report emulator region on new run results in the run viewer details pane.
- 4f24aea: Make editor floating step card draggable
- ef7f299: Change conditionals to show the status of the conditional not the conditional and substeps.

## 0.73.2

### Patch Changes

- 1d986d8: Improve reliability of AI response streaming for OpenAI-based completions

## 0.73.1

### Patch Changes

- 66fdd71: Improve observability for mcp traces.
- 295d49f: Kill App step now dismisses notification overlays before killing the app, retrying up to 5 times
- 8c5a78b: Properly cancel in-progress runs on sigterm

## 0.73.0

### Minor Changes

- eb33742: Add iOS video recording support. Videos are automatically captured during test runs and stored in the run attempt assets.

### Patch Changes

- 296e1d7: Address security vulnerabilities
- 40d3461: Make the platform and version visible with the emulator region for remote emulators.
- 2cc694f: Fix bug where SCROLL_TO on iOS where repeated cache resolution attempts could cause unnecessary scrolling.
- 2cc694f: Fix bug where SCROLL_TO could place the element near the bottom of the page where it was covered by the bottom bar
- 2cc694f: Increase default scroll speed and height

## 0.72.0

### Minor Changes

- 75c67b3: Add "Run to" and "Run from" context menu options for steps in the mobile editor to execute from the start of a section to a step, or from a step to the end of a section

### Patch Changes

- aa38559: Ignore .momentic-mcp from globbing

## 0.71.1

### Patch Changes

- a6390d8: Add keyboard navigation handler for mobile editor
- b303346: Prevent unnecessary appium liveness checks
- 7259435: Improve error collection
- 782c501: Fix git repo detection to work in repositories with no commits.
- 51908d6: Use exit code 1 for all test cancellations
- 2ce4ca3: Add Bitrise CI detection for automatic git metadata extraction
- 51908d6: Emit correct status when runs fail due to mid-execution timeout
- 412e5ea: Prevent timeouts when typing really long text

## 0.71.0

### Minor Changes

- baf8991: Add traces for AI extract step

### Patch Changes

- 8da3f1b: Improve the momentic-test skill's ability to use variables in Momentic.

## 0.70.0

### Minor Changes

- 0fd3520: Store mobile screenshots with the correct png extension
- 5cfd805: Add support for executing Appium commands on iOS

### Patch Changes

- f39aa3c: iOS screen checks now also inspect webview content using safari scripts

## 0.69.0

### Minor Changes

- b4b3fa8: Update editor UI to be single step list panel with output, and floating step editor form

### Patch Changes

- df04bf5: Fix a race condition that caused emulators to be orphaned if the user CTRL+C-ed too quickly after emulator creation
- 65773a0: Remove unnecessary error logs from local app
- 65773a0: Stop writing unnecessary fields when creating new tests
- a392554: Display setup and teardown sections in run viewer
- b6e232d: Add context pane data for mobile test results in the run viewer

## 0.68.1

### Patch Changes

- 252a97e: Fix iOS bug where scrolls were happening too fast, causing some momentum to remain after scrolling and swiping
- eef0563: Retry cache resolution until timeout on iOS cached path for smarter waiting
- ec23fd3: Further increase default scroll attempts to 15
- 7907503: Make iOS device type a select when configuring local emulator options
- 7907503: Return a better error message when an invalid device type is specified for local iOS emulators

## 0.68.0

### Minor Changes

- ba179dc: Fix several SCROLL_TO positioning bugs that caused caches for SCROLL_TO to bust unnecessarily and improve SCROLL_TO performance for both iOS and Android
- ba179dc: Improve AI Action intelligence by upgrading models and prompts

### Patch Changes

- 243d779: Fix bug where SCROLL_TO sometimes stopped scrolling too early for small containers
- 243d779: Loosen timeouts for screenshots and page source get calls to account for periods of emulator provider instability
- ba179dc: Increase default scroll attempts from 5 to 10

## 0.67.4

### Patch Changes

- e13c020: Fix flags passed to the app start command
- 184b3b4: Enable element checks for iOS webviews

## 0.67.3

### Patch Changes

- c6ef783: Fix calculation of relative element coordinates within iOS webviews

## 0.67.2

### Patch Changes

- 1b75fc3: Fix issue where scroll to failed step would sometimes scroll ancestor scroll container

## 0.67.1

### Patch Changes

- 1cb630f: Fix issue where conditional step output in run viewer would cause page error

## 0.67.0

### Minor Changes

- 65b7ad9: Add local emulator support for iOS
- 8869d7b: Added conditional step for editor

### Patch Changes

- 7a46a4f: Retry failed appium commands during Android test execution
- 7c138eb: UI for changing local iOS device options
- 21dcfdb: Retry failed appium commands on iOS

## 0.66.0

### Minor Changes

- 5ab30f1: Add setup and teardown sections

### Patch Changes

- 4ec5f84: Fix bug with failure recovery not properly saving retried steps' results to the environment.

## 0.65.0

### Minor Changes

- e506d2b: Add CLI flags to override region for mobile editor sessions

### Patch Changes

- e506d2b: Increase timeout for Android app installation to reduce emulator creation errors

## 0.64.0

### Minor Changes

- 0ca53a6: Android soft reset no longer clears app and device caches or device settings

## 0.63.2

### Patch Changes

- 953296d: Improve mcp trace observability.
- 54a5a7e: Improve input validation for the open app step

## 0.63.1

### Patch Changes

- bc5fc8a: Improve mcp session logging.

## 0.63.0

### Minor Changes

- 07821c5: Change install-skills to do local installs instead of global.
- 3a858d1: Add support for executing adb commands in android tests
- 66862b0: Changed the install-skills command to use --editor [your editor] instead of ide specific flags.

### Patch Changes

- 66862b0: Ship skill markdown as a file asset under skills/ instead of inlining via process.env substitution
- 5a4a5bc: Add spans to mcp and add span output artifact on session terminate tool.
- 4891204: Fix alignment of step indices on run viewer

## 0.62.0

### Minor Changes

- 808091e: Open up a headful emulator UI when creating mobile MCP sessions by default.

### Patch Changes

- 9b1b3f6: Disable xml snapshots by default for mobile runs
- 808091e: Fix issue where opening Chrome would sometimes show only a small corner of the page.

## 0.61.1

### Patch Changes

- adb892d: Update engines to be consistent with existing requirements
- b9ef0cb: Use more performant methods for basic actions

## 0.61.0

### Minor Changes

- 260b9e4: Add run URL and attempts fields to the buildkite reporter

## 0.60.1

### Patch Changes

- f7cc3e2: Change default element check condition from "exists" to "is visible"

## 0.60.0

### Minor Changes

- 42d95af: Add ability to delete a test from the test details pane in the mobile app

## 0.59.1

### Patch Changes

- 5faf16b: Allow swiping on webviews
- 5faf16b: Allow typing into webviews
- a2a574a: Strip permissions from uploaded assets so that they can be installed without errors

## 0.59.0

### Minor Changes

- e7d9c14: Add support for mocking iOS geolocation

### Patch Changes

- d5474af: Improve performance of waiting for screenshot stability
- d5474af: Increase timeout for taking screenshots
- d5474af: Remove invalid regions from iOS test creation options
- d5474af: Filter out webdriver agent from apps to open

## 0.58.0

### Minor Changes

- e548fbb: Add relative coordinates support to SWIPE step for both iOS and Android platforms
- 3d10517: Update prompts for iOS locator, assertion, and AI Action
- 30701a9: Inject variables into AI action instructions on mobile

### Patch Changes

- 3cb2a73: Fix issue where you could not clear target description field on type step
- 631bfc9: Hoist before/after screenshots for mobile AI action steps from sub-steps

## 0.57.0

### Minor Changes

- 3e0591e: Release iOS testing in beta
- 480a951: Add support for iOS modules.

### Patch Changes

- 17fe56c: Fix a bug where appium would fail to register drivers if running with the --parallel flag.
- 7a00b75: Change the splice tool to return a recovery artifact to enable agents to undo bad splices accurately.
- 6a7caae: Improve the skill to improve the model's usage of cache keys to persist caches from previewed steps.

## 0.56.0

### Minor Changes

- 1955db3: Add --java-home and --android-home flags to the mobile mcp to enable mcp usage in codex.

### Patch Changes

- cdfbc66: Resolve issues with hanging black Apple logo screen
- cdfbc66: Improve the performance of typing on iOS

## 0.55.1

### Patch Changes

- 3d70ff6: Harden the mcp to prefer remote emulators even more.
- 8d41b69: Tune the session creation tool to default to the test's default emulator then primarily remote emulators. The model using the mcp tool should only use local emulators when directly requested.
- 77924aa: Improve the session start tool to return the installed applications
- 77924aa: Improve the get environment variables tool to also return a file link to an installed applications report.
- 77924aa: Auto filter the available applications in IOS tests.

## 0.55.0

### Minor Changes

- 1e7e990: Add the install-skills command to the mobile cli package.
- 2c49514: Rename the get attributes tool to get artifacts and updated the momentic-test skill.

### Patch Changes

- d4344e0: Fix cache consistency enforcement for iOS
- 4f3602f: Add labels to the get attributes channels file artifact output and improve descriptions for more accurate test creation.
- 0515419: Update the skill to not push through errors when the session has clear errors.
- f6de50e: Improve the skill to prevent the model from over using javascript steps for actions native momentic steps already perform.
- 5fa34ba: Tune tool descriptions to encorage better model behavior when editing.

## 0.54.0

### Minor Changes

- 893e28a: Removed the momentic_module_list tool from the mcp and moved its functionality to the get attributes tool.
- 893e28a: Renamed the momentic_attributes_list to momentic_get_attributes.

### Patch Changes

- 893e28a: Improved the error handling and description of the get attributes tool.
- 893e28a: Improved the momentic-test skill to better understand the get attributes tool.

## 0.53.1

### Patch Changes

- a5c98fc: Upgrade the mobile mcp get attributes tool to return the availableChannels for the model to select for test creation.

## 0.53.0

### Minor Changes

- 4a3c90f: Add the preview step tool to the momentic mobile mcp.
- b850fcf: Add the get initial data tool for mobile mcp.
- fe5c302: Add the splice tool to the momentic mobile mcp server.

### Patch Changes

- 889afe5: Update run viewer details panel styles
- de63f5c: Improve response message to the model when cache entries fail to save inside the mcp's splice tool.
- e749e10: Sentence case step type names (AI check, Element check, Page check) across UI labels, error messages, and agent prompts
- d8d300e: Change the mcp step parser to accept --_-fraction instead of --_-percentage to fix the misnomer.

## 0.52.1

### Patch Changes

- 42fc41e: Fix support for conditional commands in the run viewer
- 4a7f565: Make relative element cache checks stricter
- 4a7f565: Fix a bug where some required elements were incorrectly failing relativity checks

## 0.52.0

### Minor Changes

- 1d33d67: Improve Android page retrieval speed
- 1d33d67: Turn on Appium's "simpleBoundsCalculation" flag for Android emulators by default to avoid hanging page fetches

### Patch Changes

- e69d482: Add query param for displaying detailed traces

## 0.51.0

### Minor Changes

- 90dbec5: Add --session-idle-timeout-minutes flag and MOMENTIC_SESSION_IDLE_TIMEOUT_MINUTES env var to configure MCP session idle timeout

### Patch Changes

- da6baed: Display the actual connected limbar region in the mobile editor device preview
- 9164f71: Filter channels and tags by platform in edit mobile test options dialog
- c22e44c: Split asset details into separate Channel and Tag sections
- 4d89166: Exclude failure_section tag from buildkite JSON report for non-failed tests
- 38ec4a1: Minor UI updates on run viewer step list
- 3ccb48d: Revert --port flag to use PORT env var instead of MOMENTIC_PORT
- 96e97fe: Prevent InlineCode from shrinking in run viewer step content by adding shrink-0
- d31368a: Hide Add File step for iOS

## 0.50.0

### Minor Changes

- 12338df: Support running the local app on a custom port via --port flag or MOMENTIC_PORT env var
- f52e2b1: Add support for iOS app launch arguments

### Patch Changes

- bb29d92: Fix so steps are unselected when closing step details panel
- fc73131: Minor UI organization for step details panel

## 0.49.1

### Patch Changes

- 049e435: Fix Open App packages input requiring two clicks to type by preventing Radix Popover from stealing focus on open

## 0.49.0

### Minor Changes

- 9c486cb: New buildkite-json reporter for run granularity reporter data for buildkite.

### Patch Changes

- 05b8d58: Handle Appium driver manifest race condition: retry on 'Multiple drivers claim' error in addition to 'Could not find a driver' error
- 9c486cb: Fix junit reporter to properly identify whether a step failed in setup, main, or teardown.
- 388c254: Fix drag hover duration for iOS

## 0.48.1

### Patch Changes

- 6cbf592: Fix scroll-to-target failing after scrolling element into view
- 5956c7b: Improve reliability of iOS rotate orientation step
- 73fbf9b: Fix iOS type steps failing with repeated characters
- ce26cdd: Fix for not being able to add mobile parameters and parameters not being replaced in template expressions
- 5956c7b: Fix cache/memory eviction on iOS

## 0.48.0

### Minor Changes

- e80c6b6: Remove "Debug state" step type from the add step selector.
- deac80f: Add remote emulators to the mobile mcp.

### Patch Changes

- 1d46d33: Speed up code paths that fetch Git metadata for the current user and branch before the test editor opens
- a3bc4b2: Prevent soft reset during ongoing execution on mobile
- fb80f3d: Update display of Add File step output directory
- ce4dd29: Fix soft reset killing WebDriverAgent and Appium apps on iOS

## 0.47.0

### Minor Changes

- 1098b96: enable ios ai action support

## 0.46.1

### Patch Changes

- c4f5ed9: Update run details panel to be detachable and error text easier to read
- f675781: Fix the bug where if a run step tool call took more than 5 min the session would be purged.

## 0.46.0

### Minor Changes

- 5b03448: Add the disable cache option flag on the mcp command to enable disabling caches by the mcp, with proper validation at the command level.

## 0.45.0

### Minor Changes

- 3f88169: Add the save cache option flag on the mcp command to enable force cache overwrites by the mcp.
- c91cc09: Added the get environment variables tool to the momentic mobile mcp.

### Patch Changes

- 4ffebd1: Fix issue where tests page scroll position reset when opening test details panel
- 89d3205: Fix iOS driver version mismatch errors
- dd72399: Fix emulator soft reset to also reset the test's environment variables.
- b27f822: Add wait for stability span and change previous wait for stability description to smart waiting
- b541fd6: Update resources tab on run viewer to have split charts for cpu/memory
- c91cc09: Adjust the cache saving for mcp servers to not overwrite caches on main when executing run step.

## 0.44.0

### Minor Changes

- b67f4a5: Remove the get test tool and instead pass the path to the yaml to be more token efficient.
- b67f4a5: Add the run_step tool to the momentic mobile mcp.
- 7dcbe42: Add the get session state tool the the momentic mobile mcp.
- f1e5752: Add iOS scroll to command

### Patch Changes

- b1dd5a4: Add iOS element check step
- cc57461: Add iOS platform-specific command defaults and hide iOS-incompatible buttons in editor UI
- f03fea2: Improve the response from the momentic start session tool and improve the get browser state output by adding a fallback screenshot attempt and improved handling for failed xml state outputs.

## 0.43.0

### Minor Changes

- b1bf0e8: Add drag and drop support for iOS
- 41d1b2a: Allow SCROLL TO steps to customize maximum scroll attempts

### Patch Changes

- 2c21cf6: Retry appium server start for iOS tests
- 8122b67: Adding a new step in the editor will scroll the step into view
- aa3372a: Add env output field to javascript step

## 0.42.0

### Minor Changes

- 756a3c3: Fix instances where failure recovery would suggest retrying the failed step itself unnecessarily.
- 756a3c3: Allow AI Action to generate coordinate-based targets based on the input goal
- 756a3c3: Fix instances where failure recovery would suggest retrying the failed step itself unnecessarily.

## 0.41.0

### Minor Changes

- 065d164: Add kill app support for iOS
- 2c142f4: New momentic mcp tool for creating tests.
- 4e4cc92: Session start and terminate tools for the mobile mcp server.
- 4f8d041: Rename momentic_test_environment_list to momentic_attributes_list with structured output.
- 0ff203e: Implement press keyboard for iOS
- ff84a5c: New create module tool for the mobile mcp.
- 4365fd5: Add cross-platform ADD_FILE command for iOS
- 967436f: Add cross-platform screen check support for iOS

### Patch Changes

- ff84a5c: Add support for absolute paths to tests in the create module tools.

## 0.40.0

### Minor Changes

- 13aa0b1: Momentic mobile mcp now has access to a tool to list all module headers.
- 14994a9: feat: add iOS swipe step
- cdca717: Momentic mobile mcp now has access to a tool to retrieve modules via selectors.
- ffc2245: New momentic mobile mcp tool for fetching a specific test via a selector.
- 3ca3155: New momentic mobile-mcp tool for listing tests and environments present on your machine.
- 3454a30: Added the mcp command and stdio mcp server to momentic mobile.

### Patch Changes

- ce1a262: Add JAVASCRIPT, WAIT, REQUEST, and ROTATE_ORIENTATION command support to the iOS controller

## 0.39.3

### Patch Changes

- 0e401fb: Support clear content for iOS type steps
- 45b4d64: Add iterations and tapDelayMs support to iOS tap performer

## 0.39.2

### Patch Changes

- 8a78b7f: Add images to AI assertion and locator traces for run viewer

## 0.39.1

### Patch Changes

- 0fefab8: Filter folder listings in mobile CLI to only show mobile tests and modules (and vice versa for the desktop CLI)

## 0.39.0

### Minor Changes

- a6d084f: Hide non-iOS steps from the editor for iOS tests

### Patch Changes

- a6d084f: Get screenshot before accessibility tree to avoid race conditions where the two are out of date

## 0.38.3

### Patch Changes

- 3f91646: Add caching for native targets in iOS

## 0.38.2

### Patch Changes

- 657440c: Hide Android-only options in test options dialog for iOS tests

## 0.38.1

### Patch Changes

- fae65d2: Fix issue where mobile AI failure recovery steps were not correctly labeled in UI

## 0.38.0

### Minor Changes

- 9757644: Add AI Extract to mobile.

## 0.37.2

### Patch Changes

- 2984701: Fix bug where local app exits on non-critical errors

## 0.37.1

### Patch Changes

- c6fa1e9: Fix a bug where sigint was unhandled for desktop servers
- 30142c1: Simplify tooltip copy

## 0.37.0

### Minor Changes

- ca92267: Add support for isolating step caches by environment

## 0.36.6

### Patch Changes

- abed478: Minor UI fixes

## 0.36.5

### Patch Changes

- c40e39c: Always show run link input field when run group request fails in the local run viewer
- 5ebc821: Run viewer and mobile editor layout fixes

## 0.36.4

### Patch Changes

- 43e9d4d: Add more logger context (orgId, parentStepIdChain, platform) to mobile step cache eviction log messages

## 0.36.3

### Patch Changes

- 0b9fdb3: Fix issue with video recording timestamp being off after switching tabs during high machine resource usage

## 0.36.2

### Patch Changes

- 054e94e: Fix issue where run viewer steps would not collapse if selected
- 054e94e: Fix issue where editor steps would not collapse if selected

## 0.36.1

### Patch Changes

- f54591f: Fix issue where save action was called upon initial test load

## 0.36.0

### Minor Changes

- 26bb35f: Update run viewer to use new hierarchy structure for nested steps
- 26bb35f: Update editor to use new hierarchy structure for nested steps

### Patch Changes

- b7bec68: Pressing Escape closes the details panel when viewing a row (tests, suites, files, test plans, run groups).

## 0.35.6

### Patch Changes

- 49da689: Limit width of tooltips in video player

## 0.35.5

### Patch Changes

- 57dac0a: Fix issue where unbroken words in editor results caused element overflow

## 0.35.4

### Patch Changes

- 03d78db: Change orientation of label for run viewer step settings that include code blocks

## 0.35.3

### Patch Changes

- 9983451: Fix overflow issue when resizing local run viewer

## 0.35.2

### Patch Changes

- 7cb2c54: Fix overflow issue when resizing local run viewer

## 0.35.1

### Patch Changes

- 5818d33: Update UI for failure recovery steps

## 0.35.0

### Minor Changes

- bdd0757: Update mobile reset button styling and call it "Soft Reset"

## 0.34.2

### Patch Changes

- b3099d1: Fix issues with run Viewer UI

## 0.34.1

### Patch Changes

- 642ae79: Fix issue where OPEN_APP selection was not immediately saving

## 0.34.0

### Minor Changes

- 3076456: Update Run Viewer UI to match mobile editor experience

## 0.33.4

### Patch Changes

- c6f0f27: Improve error handling in environments where git is not installed

## 0.33.3

### Patch Changes

- 43c4fa9: Improve error reporting

## 0.33.2

### Patch Changes

- eb74162: Capture more exceptions for internal reporting

## 0.33.1

### Patch Changes

- 0998aa7: Fix issue with step edit panel toggling when expanding to view module children

## 0.33.0

### Minor Changes

- 97ebb47: Adds ability to reset android emulator.

## 0.32.1

### Patch Changes

- 14a3bba: Fix the minimum width of the navigation bar in the local app

## 0.32.0

### Minor Changes

- 2f5ed8a: Add backend support for iOS test execution

### Patch Changes

- 74fd5f5: Fix use-editor-state getUniqueId call
- c41dd02: Fix caches not saving for mobile tests run on the cli
- b3783ec: Fix issue where editor was saved when first loaded with no changes

## 0.31.2

### Patch Changes

- 81f8526: Ungate the feature to detect element targets that change mid-interaction (part of the last minor release)

## 0.31.1

### Patch Changes

- 1a3df3b: Add editor options for change emulator orientation
- 4d54e1e: Fix issue where toggling through test details panels would not update test name input value

## 0.31.0

### Minor Changes

- b1afdff: Improve interaction model to detect element targets that change mid-interaction and retry execution.

## 0.30.1

### Patch Changes

- 247ad9f: Fix a sharding bug where some shards included duplicate items

## 0.30.0

### Minor Changes

- ad9fcf4: Show AI settings in run viewer

## 0.29.0

### Minor Changes

- 35dce4f: Capture before and after XML state for mobile tests by default. Can be turned off with test setting
  Update accessibility language and tab in mobile editor to screen xml

### Patch Changes

- 6348cf4: Fix UI bug where selecting Long Press on tap step would not update step list content displayed

## 0.28.0

### Minor Changes

- 5953418: Show webview traces within mobile trace
- 1f7e786: Adds quarantined_at to CLI and Mobile CLI report outputs

### Patch Changes

- 8eb6014: Improve android webview detection

## 0.27.0

### Minor Changes

- a2f8bcd: Record system and process memory and cpu resource data during text execution and display in Run Viewer

## 0.26.1

### Patch Changes

- 43b0ba0: Fix a bug where element checks on attributes that do not exist pass

## 0.26.0

### Minor Changes

- 42e6e61: List runs on landing page for local run viewer and make runId optional in results view command

### Patch Changes

- 296bc95: Improve enforcement of relative elements in caches
- c0fdd3d: Pin appium-uiautomator2 package as it breaks with higher version of appium

## 0.25.1

### Patch Changes

- 7fc78d8: Fix playwright dependency installation on windows
- 9ff9bd1: Add field-level validation to editor step inputs

## 0.25.0

### Minor Changes

- 244330c: Add results view command to launch local run viewer and view local results

### Patch Changes

- 48fecad: Hide incorrect credit estimate from the test details pane
- eca74d8: Step selection defaults to ordered by alphabetical order.
- 48fecad: Sort modules alphabetically when creating a new step
- 48fecad: Fix an issue where cleanup would fail after creating test results archives due to open file streams

## 0.24.2

### Patch Changes

- 762bf2c: Fix failure recovery steps not showing as AI generated in mobile results

## 0.24.1

### Patch Changes

- b544b6b: Set engine correctly (previously cli failed at runtime)

## 0.24.0

### Minor Changes

- 976ff82: Support triple tap option

### Patch Changes

- 4520016: Patch minor security vulnerability with diff-lines

## 0.23.0

### Minor Changes

- fdfa6bf: Be able to view tests that are using a module when viewing a module in the app
- 6553022: Add undo/redo functionality for mobile editor

### Patch Changes

- 9e40a82: Improve handling of ambiguous global locator redirect cases

## 0.22.2

### Patch Changes

- 5c53417: Catch invalid test file schema errors when launching local app

## 0.22.1

### Patch Changes

- b440950: Use PNGs for failure recovery
- 5faca04: Support --region flag when running mobile tests, which can be used to force the tests to run remotely or locally. This can be useful when using different setups for development and CI.

## 0.22.0

### Minor Changes

- 25038dc: Support duplicating mobile tests from the editor

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
