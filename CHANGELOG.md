# momentic-mobile

## 1.6.6

### Patch Changes

- 620d825: Modules are expanded by default when added via the step picker
- c552c9f: Gracefully handle system dependency installation failures (e.g. spawn su EACCES) during browser setup instead of crashing

## 1.6.5

### Patch Changes

- 0164f00: Fix saving of tests with long multi-line JavaScript steps introducing unwanted line breaks in the code

## 1.6.4

### Patch Changes

- 2338385: Improve AI agent guidance around step cache usage

## 1.6.3

### Patch Changes

- 2cc87df: Fix layout issue in editor step list causing element overflow

## 1.6.2

### Patch Changes

- c98a9e1: Pressing Escape in the editor now dismisses one layer at a time — a layered modal or a focused input is cleared before the side panel closes.

## 1.6.1

### Patch Changes

- a1be78f: Fix Run To in editor to resume after last executed step instead of re-running from the beginning

## 1.6.0

### Minor Changes

- 6dac91a: Support running only multi-selected steps via context menu or keyboard shortcut

## 1.5.1

### Patch Changes

- a87f5b0: Allow passing an optional timeoutSeconds to momentic_poll_runner to wait for active runs to finish.
- af61e64: Modules are expanded by default when created

## 1.5.0

### Minor Changes

- 87661b6: Add a soft timeout to momentic_run_step which responds after 30 seconds with the currently executing step and how to poll for the result
- 87661b6: Add momentic_poll_runner tool which responds with the status of executing steps on the session
- 87661b6: Significant skill update for how to handle the new run step status tool and polling pattern

## 1.4.7

### Patch Changes

- 151f2cd: Auto-scroll step list to keep the executing step in view during test runs

## 1.4.6

### Patch Changes

- 465a07e: Fix collapsed conditional steps unexpectedly expanding during test execution
- 44bf5b5: Restore editor autoscroll behavior for streaming step output.
- d4fadc2: Round scroll pixel values in trace display

## 1.4.5

### Patch Changes

- 9d99843: Pause editor trajectory autoscroll while users are scrolled away from the bottom.
- d70920c: MCP server now cleans up active sessions and emulators when the MCP client disconnects

## 1.4.4

### Patch Changes

- 231dd9d: Fix issue introduced in 91a9ddb that caused test saving and the auto-save indicator not to work in the local editor on the initial load

## 1.4.3

### Patch Changes

- be1fef2: Keep the MCP daemon alive while long-running steps are executing

## 1.4.2

### Patch Changes

- 272c754: Fix folder dropdown scroll behavior in create module and move dialogs

## 1.4.1

### Patch Changes

- 91a9ddb: Simplified v2 YAML output no longer includes schema version metadata, default viewport (1920x1080), or default browser type (Chromium).

## 1.4.0

### Minor Changes

- 08af958: Support autoAcceptAlerts, autoDismissAlerts, language, and locale emulator settings
- 5afbdfe: Make taps more resilient to elements moving mid-action.

### Patch Changes

- 0d596ed: Improve mobile AI Action recovery when cached app content changes.

## 1.3.5

### Patch Changes

- 43bc4aa: The momentic, momentic-mobile, and wizard CLIs now require Node.js ^22.12.0 || >=24.0.0 and exit at startup with an actionable message when run on an unsupported version.

## 1.3.4

### Patch Changes

- 8b40178: Update notification now shows the version you'll actually upgrade to and warns when it's a new major version with potential breaking changes
- e6831ad: Make browser installation more reliable: re-install partially-downloaded browsers instead of later failing with "browser is not installed", and fix garbled progress output during the download.

## 1.3.3

### Patch Changes

- 1554b9a: The "update available" notice now links to GitHub Releases for the changelog.

## 1.3.2

### Patch Changes

- f272efd: Wait for iOS keyboard input readiness before typing.

## 1.3.1

### Patch Changes

- 9734965: Fix knowledge base citation links in the local run results viewer to correct url

## 1.3.0

### Minor Changes

- 59ee659: Add JSON run reporter

## 1.2.0

### Minor Changes

- 376c802: Add element locating to the mobile editor so you can find matching on-screen elements from a target description.

### Patch Changes

- 6ee2d10: Fix a broken-image placeholder appearing in the mobile editor device preview while the emulator is booting
- db466c1: Fix iOS taps that could fire before a remote simulator finished booting; mobile runs now wait for the device to be fully booted before executing steps.
- 29f2a2b: Fail fast with a clear error when the CLI is run on an unsupported Node.js version.

## 1.1.2

### Patch Changes

- 3f1ab24: Fix an issue where scroll actions could tap instead of scrolling

## 1.1.1

### Patch Changes

- c7e63cd: Show a clear validation error when an iOS test uses a command or key that isn't supported on iOS, instead of failing with an unexpected error
- 5f1426a: Fix an unexpected error when running a mobile test that references a module containing an invalid or unsupported step. These now report a clear validation error instead of failing with an internal error.

## 1.1.0

### Minor Changes

- 282b299: Add Allure report support (allure, allure-json) to the mobile CLI for iOS and Android, matching the web reporters.

### Patch Changes

- 7e5f725: Fix mobile device sessions failing to start with `UND_ERR_INVALID_ARG` on Node.js 26 and newer.
- 36f4221: Fix the iOS Add File step so preset storage locations like Photos can be picked from the dropdown without reverting to a custom path
- 728f472: Clarify ADD_FILE --storage-location guidance in the mobile Step Authoring Guide (iOS Photos library import vs app sandbox container, Android media directory)
- c5a2626: Smooth out the run progress spinner animation

## 1.0.4

### Patch Changes

- ab638ce: Show a clean, actionable error message instead of a stack trace when a command fails with an expected error such as an unknown run group or run ID.

## 1.0.3

### Patch Changes

- 693f21d: Resolve security advisories in bundled dependencies.
- 4081c30: Editor Run button is now a split button to choose which sections (Setup, Main, Teardown) to run.

## 1.0.2

### Patch Changes

- cce9b28: Fix the Visual Diff step's threshold field in the mobile editor so it accepts the full range of values (shown as a percentage) instead of snapping to only 0 or 100%.
- 595b021: Fix the run viewer's expand-editor modal so the code editor fills the modal height

## 1.0.1

### Patch Changes

- 2c7e648: Editor tab filters (Console, Network, and others) now persist when switching between tabs, clearing only on page refresh

## 1.0.0

### Major Changes

- 209ade0: Dropped support for Node.js 20, which has reached end of life. The CLIs now
  require Node.js 22 or newer.

### Minor Changes

- 209ade0: Test run videos now default to `on-fail`: a recording is captured for every run
  but kept only when the test fails. Pass `--video true` (or set `recordVideo: true`)
  to keep every recording, or `--video false` to disable recording entirely. The
  deprecated `--record-video` flag has been removed — use `--video` instead.

### Patch Changes

- 209ade0: Updated the bundled Playwright to 1.60.0, picking up the latest browser engines
  and upstream bug fixes.
- 209ade0: New projects now default to the latest version of each AI agent, pinned to an
  exact sub-version. Pinning keeps the default from changing unexpectedly when a
  newer revision of the same agent ships. Existing projects that already set
  `ai.agentConfig` are unaffected.
- 209ade0: AI Action steps now default to the V3 agent everywhere. The older V2 agent is marked "Legacy" and can no longer be selected for new AI Action steps in the editor; existing V2 steps continue to run.

## 0.116.2

### Patch Changes

- d73b634: The CLI now shows important announcements from Momentic after checking for updates.

## 0.116.1

### Patch Changes

- 2319d19: Improve the reliability of AI Action when extracting data from scrollable lists and working with environment variables.
- 88688c7: Fix mobile CLI dependency resolution so the package installs and publishes reliably
- 35a3a7e: Show a clear validation error instead of an internal error when a mobile test file uses an unsupported or invalid command.

## 0.116.0

### Minor Changes

- 392ffc9: Add visualDiff command for mobile tests: compare a full-screen screenshot against a local golden image, with a configurable threshold. Goldens are created on first run and updated with --update-golden-files.
- 57a8f40: Improve reliability of Android mobile test runs by ensuring the remote emulator's Playwright server matches the CLI's Playwright version.

### Patch Changes

- a66d503: Patch a critical security vulnerability (CVE-2026-9679, CRLF injection) in an underlying HTTP networking dependency.

## 0.115.0

### Minor Changes

- e7068f1: Fix clearing and replacing existing text when typing into native and webview inputs on iOS and Android, including protected and secure fields.

### Patch Changes

- e2a2716: Fix issue with two interaction highlights on mobile web
- 291bba9: Fix run viewer video player sizing issues, add spacebar keyboard shortcut for pause/play
- 4064902: Keep running when project configuration cannot be reloaded after a file change (e.g. a temporary network issue); the previously loaded configuration is kept instead of surfacing an error.
- 82ccff9: Dragging a step over a collapsed module or conditional now auto-expands it after a brief hold, so you can drop steps directly inside. It re-collapses if you drag away without dropping.

## 0.114.0

### Minor Changes

- c5c8698: Implement additional content replacement strategies for Android/iOS. By default, Momentic will attempt all of them one by one until the text is cleared.

### Patch Changes

- 546d7ae: Mobile AI checks now support a visual-only assertion mode that evaluates the screen using the screenshot alone, without the accessibility tree

## 0.113.0

### Minor Changes

- e1fd29b: Add key press delay and repeat support to the mobile PRESS KEYBOARD step (ENTER/BACKSPACE) on iOS and Android.

### Patch Changes

- ed9a584: Fix mobile AI action runs sometimes showing an empty agent trajectory in the editor, and show the correct AI action version in the run viewer
- 59b662d: Improve reliability of run telemetry delivery on networks with restricted egress

## 0.112.1

### Patch Changes

- f548a40: AI Action can now perform a wider range of actions when generating mobile steps, including extracting data, rotating the device orientation, and running JavaScript.

## 0.112.0

### Minor Changes

- bf0a6b4: Add ability to ungroup a module instance in the editor, inlining its steps in place

### Patch Changes

- f8f56fa: Mobile run details in the run viewer now show the emulator OS version (e.g. "Android 14", "iOS 26") for remote runs.
- ae2e6dd: Fix a rare error that could cause AI Action steps to fail to complete

## 0.111.1

### Patch Changes

- 3fededd: Automatically retry mobile emulator setup once on a fresh emulator when device bringup fails, and tighten setup timeouts so a slow start fails fast instead of stalling. iOS tests now also stop quickly when the device becomes unreachable mid-run instead of grinding through retries against a dead device.
- 338eb6c: Fix `install-browsers` so installed browsers are no longer unexpectedly removed when another Playwright-based tool shares the same browser cache, which previously caused "required browser executables are not installed" errors when running tests.

## 0.111.0

### Minor Changes

- 8d0fd93: Add support for additional remote emulator regions (us-east1, us-east2, us-west2) for mobile test runs
- c25036e: Add continent-level emulator regions (us, eu, as) that automatically run on the closest available region within that continent. iOS is supported in us and eu.

## 0.110.1

### Patch Changes

- 1e53ab9: When a required browser isn't installed, the error now names the missing browser and gives the exact command to install just that browser. Command suggestions printed by the CLI now include a runnable prefix so they can be copy-pasted and run directly.
- ec1e633: Fix missing spacing between fields and sections in the app's dialogs and panels

## 0.110.0

### Minor Changes

- 320bda0: The v4 locator, assertion, and visual-assertion agents are now the recommended default. New projects use them automatically, and existing projects that don't pin those agents in `ai.agentConfig` will pick them up as well. v4 is faster and more reliable than v3.

## 0.109.3

### Patch Changes

- 12a53df: Show clearer error message when runs are blocked due to usage limits
- 5a0aa97: Mobile run details now show the asset tag the test ran with, including runs started from a channel without an explicit tag.

## 0.109.2

### Patch Changes

- a1b1567: Show individual AI Action sub-steps in the run viewer for mobile test runs

## 0.109.1

### Patch Changes

- 218eff3: Improve reliability of AI Action v3 mobile healing
- 6d92514: Show a clear, file-specific error when a test or module file contains invalid YAML, instead of an unexpected crash.

## 0.109.0

### Minor Changes

- 269ed59: AI Action V3 mobile steps now support optional pre-conditions and post-conditions.
- a15bcf0: Add a --share-diagnostics flag to share local mobile run diagnostics via OpenTelemetry

### Patch Changes

- 37aaf86: Show the failure reason for each failed test in `momentic-mobile run` output, making local runs easier to debug

## 0.108.0

### Minor Changes

- b04a91c: Add ability to drag and drop multiple steps at once in the mobile editor

## 0.107.0

### Minor Changes

- f3bbe94: Show inline screenshots in the mobile editor's live AI Action v3 agent trajectory as it runs

### Patch Changes

- 17a0807: Show a clear, actionable error when renaming or creating a test with a name that already exists, instead of an unexpected internal error
- 0f24f57: Don't block iOS test runs when Android tooling (Java, ANDROID_HOME, ADB) is missing; these are now non-blocking warnings
- f3bbe94: Fix bug where iOS AI Action v3 trajectory was not shown in the run viewer
- dc37480: Add diagnostic tracing for AI actions to improve observability of mobile test runs
- fd3af98: When the mobile driver fails to start, the underlying Appium startup error (for example, an unsupported Node.js version) is now shown instead of a generic failure message.
- c9227e5: Fix the step editor panel sometimes not appearing when selecting a step in the mobile editor after the panel had been resized closed
- 74aa15c: Show a clear, actionable message instead of an unexpected crash when sign-in credentials can't be saved due to file permissions

## 0.106.2

### Patch Changes

- d1eb26a: Fix issue where empty folders would not show up when choosing folder to create or move a module

## 0.106.1

### Patch Changes

- 84e2094: Add a folder picker when creating a module in the mobile editor, so you can choose where the new module is saved (defaults to the current test's folder)
- 9dda778: Fix issue where panels would not persist layout through certain interactions
- fd0bea3: Clearer error when opening an app that isn't installed on the device, distinguishing a missing app from one with no launchable activity
- 6b0e305: Improve reliability of installing apps on iOS devices

## 0.106.0

### Minor Changes

- 9b3494b: Add knowledge base access to failure recovery agent

### Patch Changes

- 39ffd14: Update bundled dependencies to address a critical security vulnerability.
- d1398fa: Fix duplicating a step in the editor producing a duplicate command ID that failed the duplicate-IDs check on v1-format projects
- bd630fd: Fixed iOS Type steps silently succeeding when the system keyboard never opened after tapping the target (e.g. typing into a Safari web view search box behind a dismissable overlay). The step now re-taps the target to bring up the keyboard, and only if it still never opens does it fail with a recoverable error instead of falsely reporting success.

## 0.105.3

### Patch Changes

- cc1d1a1: Show clear messages for missing, moved, or conflicting module files instead of unexpected errors.
- 6354b9f: Add indexes to step list in the editor

## 0.105.2

### Patch Changes

- 24811c5: The run viewer now shows a "Failure recovery not eligible" callout in the step list when a failed step could not be recovered, with the short reason inline.
- 4b899f8: Fix "Module is no longer on disk" error that could block saving right after creating a module from selected steps in the mobile editor. New modules are now created alongside the test that uses them.
- 527bd09: Add keyboard shortcut to delete steps (backspace)
- a01eb83: Quieter terminal output when starting the mobile editor and running tests: the startup preflight no longer prints a redundant lint success message.
- 83729f9: Fix shift to also respect j and k in the editor for selecting, shift j and k now mirrors shift down and up arrows.

## 0.105.1

### Patch Changes

- 8f123ee: Add keybindings for adding steps after (o) and before (shift+o) selected step in editor
- 8c87b5a: Fix mobile tap steps that could fail at runtime with a tap delay error after changing the tap type from double/triple back to single tap or long press.

## 0.105.0

### Minor Changes

- 1db894b: Enable AI Action v3 for iOS tests, so iOS AI actions plan the flow up front, cache resolved steps, and self-heal on failure like Android.

## 0.104.1

### Patch Changes

- 4ea60ee: fix mobile device preview in Firefox

## 0.104.0

### Minor Changes

- 48d6880: Add knowledge base access to assertion agent

### Patch Changes

- 4c792b1: Improvements for display of traces

## 0.103.2

### Patch Changes

- 5a4d0e8: Speed up mobile SCROLL_TO steps when the target is already visible or near its cached position, and stop the post-resolve correction from drifting the cached scroll distance when the scroll container is already at its extent.
- d505b14: Fix issue with editor test options dialog save button being disabled with valid form info
- a19d30d: Improve agent assertion usage to reduce unnecessary settings and brittle checks

## 0.103.1

### Patch Changes

- b251c6e: Ctrl+C now immediately cancels the CLI while it is checking your API key or resolving the project config.

## 0.103.0

### Minor Changes

- 720a3cb: Add Antigravity to the coding agents the onboarding wizard can wire Momentic into

### Patch Changes

- 2fed53f: After `init`, print accurate next steps (install editor skills, wire up the Momentic MCP, open the local editor, and docs) instead of pointing at the onboarding wizard, which does nothing once a project is already initialized

## 0.102.1

### Patch Changes

- aada171: Lint validation errors are now shown ESLint/Vale-style — `line:col  error  message  location` — with a codeframe (line numbers, `>` marker, and surrounding context) pointing at the exact line in your test/module YAML, matching the style of the run-failure trace. Unreadable Zod messages were replaced with actionable ones: invalid IDs, `coords`, and mobile percent values now say what's expected instead of dumping a raw regex or `Invalid input`. Affects `momentic lint`, `momentic checks duplicate-ids`, and the preflight checks before `run`/`app`.
- 24ce328: Show a clear, actionable message telling you to run install-browsers when a run fails because the required browser executables aren't installed, instead of a raw Playwright error.

## 0.102.0

### Minor Changes

- 5cd341c: Local iOS simulator runs now target the latest installed iOS runtime by default instead of a fixed version, with a new --local-ios-version flag to target a specific runtime.
- 567eea4: Add `login` and `logout` commands to sign in with your Momentic account and save an API key

## 0.101.0

### Minor Changes

- b1e98d6: Include citations to knowledge base entries in trace

### Patch Changes

- b0dd0c5: Update dependencies to resolve a security vulnerability.
- 2c64539: Fix the local mobile app's file browser showing an empty list of tests and modules
- 9e657df: Test runs no longer exit with a non-zero status when the only failures are classified as warn.

## 0.100.0

### Minor Changes

- 2353087: Add `--skip-quarantined` and `--only-quarantined` flags to the mobile CLI, matching the web CLI. Use `--skip-quarantined` to exclude quarantined tests from a run, or `--only-quarantined` to run just the quarantined tests.

### Patch Changes

- 142efe7: Add `momentic_test_reload` to the mobile MCP server so external agents can refresh an active session's in-memory v2 mobile test state after manual YAML edits without restarting the session.
- 2cf9721: Fix a bug where `--only-quarantined` stopped reporting exit code 1 for failures.
- 779f393: Add cancel button to run individual step button in editor

## 0.99.0

### Minor Changes

- d209b5c: Add knowledge base access to locator agent

### Patch Changes

- 4b3dec4: Patch security vulnerabilities
- 5a4e16e: Improve target cache reliability so that caches are less likely to resolve to the wrong element.
- 4237e96: Fix duplicate test action so conditional step IDs are regenerated alongside other step IDs.

## 0.98.0

### Minor Changes

- 0657473: Use knowledge base context for result classification
- b5f8fea: Ungate public documentation and CLI commands for the simplified format migration

### Patch Changes

- 452a176: Show `[recovered]` next to each test in the live results when failure recovery successfully rescued the run.

## 0.97.3

### Patch Changes

- af0d534: Add ability to run selected step in editor using Cmd+Shift+Enter

## 0.97.2

### Patch Changes

- 068d985: Javascript step on run viewer can now be viewed in larger window
- ccaa6ad: Add ability to delete multiple steps at once in the editor with multiselect

## 0.97.1

### Patch Changes

- b2f7d66: Cancelled runs (from `--timeout-minutes`, `SIGINT`, `SIGTERM`, etc.) now print their run URL and cancellation reason in the final summary, alongside failed runs — so any cancelled run can be opened in the run viewer with one click.
- 4b0f641: When sharding (`--shard-count` or `--shard-index` > 1), the post-run output now prints a `merge shards:` instruction instead of an `after upload:` run-group URL. The per-shard run group is replaced after the merge step in CI, so the original link was misleading.
- 4b0f641: Trace viewer now collapses consecutive "Smart waiting" rows into a single row with the summed duration and a `(N waits)` count, so repeated stability waits during a retry loop render as one combined row instead of many separate rows.

## 0.97.0

### Minor Changes

- 4a5da36: `momentic upgrade` and `momentic-mobile upgrade` now migrate existing projects to the v2 file format end to end. Each command installs the latest matching CLI release, flips the project file format to v2, refreshes the recommended agent configuration while preserving any pinned sub-versions, and rewrites every legacy test and module YAML through the v2 serializer. Files already in v2 are skipped, and a new `--dry-run` flag previews the migration without writing anything to disk. The narrower `momentic migrate v2-format` and `momentic-mobile migrate v2-format` commands are now publicly documented as the file-only path -- use them when you want to rewrite just the YAML files without any other config changes. The `lint`, `upgrade`, and `migrate` commands now have CLI-reference pages on the docs site for both `momentic` and `momentic-mobile`.
- 9080050: Scaffold new projects in the simplified v2 file format. `momentic init`, `momentic-mobile init`, and `@momentic/wizard` now create configs with `fileFormat: v2` and emit v2 sample tests. When the wizard finds an existing `momentic.config.yaml`, it stops and points you at `momentic upgrade` / `momentic-mobile upgrade` so the existing project can be brought to the latest format on its own.

### Patch Changes

- 90e0461: Patch critical shell-quote command injection vulnerability in transitive Appium dependencies.
- 82c5112: Reduce noise in v2 YAML output by omitting optional fields that match their runtime default (e.g. `pressEnter: false` on `type`, `skipped: false` on any step).
- d1f0b11: Surface a clear permission-denied error when deleting a folder is blocked by the operating system (e.g. macOS system-protected folders), instead of failing with a generic crash.
- d241da5: Local run viewer now preserves sidebar and panel sizes when the window is resized.
- a8810a5: MCP prefers AI Action v3 for web/android when creating AI Action steps
- f6d5e31: Show a clearer, user-facing error when a `press`, `keyDown`, or `keyUp` step is given an invalid key name (e.g. `Esc` instead of `Escape`).
- 71de7b1: Emit detailed diagnostic traces for AI Action steps when running with --share-diagnostics.
- 9e34feb: Improve AI model provider routing reliability for failure-recovery, locator, and assertion steps. Run metadata now includes a schema version so future migrations can be applied automatically.
- e9ede0c: Add ability to drag and drop between editor step list sections

## 0.96.4

### Patch Changes

- 358fa75: Improve the skills guidance in choosing between AI actions and native steps.
- 6ace1cb: Fix AI Action v3 not appearing in the mobile editor
- 358fa75: Improve the step authoring guide for model's interaction with AI ACTION steps.

## 0.96.3

### Patch Changes

- ac04b6f: Improve web cache reliability by ignoring script and style content when comparing element text.
- 3d7c646: Raise the default JavaScript step timeout to 90 seconds (was 15 seconds) and allow configuring it up to 10 minutes.
- 1065b19: Fix resource-pressure hint appearing in the middle of the post-run failure summary.

## 0.96.2

### Patch Changes

- 160a381: Restore aggressive soft reset on Android so it logs users out and clears app data
- 42c2364: Fix issue where changing editor panel layout would cause emulator to reload
- 24c5ca0: Fix a crash that could occur when opening the "Create mobile test" or "Edit mobile test options" dialogs if any uploaded Limbar asset had an empty channel or tag.
- 7f62db3: Fix issue where step panel closed when clicking in the device preview

## 0.96.1

### Patch Changes

- 0271c0c: Fix a bug that was causing iOS logs to either not appear or be extremely noisy"
- 97c4c6a: Fix long test titles overflowing and making attempt dropdown inaccessible
- 1f39581: Group assets page by channel and platform and add search.
- 0b544ca: Reject empty or whitespace-only --channel and --tag values when managing mobile assets

## 0.96.0

### Minor Changes

- 7d6c2a6: Show screenshots of targeted element in mobile trace steps side panel
- 25a0f2e: Show YAML code pointer in failure summary
- aebb86e: Add `--reporter` flag to `momentic run` and `momentic-mobile run`. Pass multiple times to combine reporters (e.g. `--reporter=list --reporter=junit`); file reporters write to `--reporter-dir`. Cloud run URLs are now clickable in supporting terminals, and end-of-run output is quieter overall.

### Patch Changes

- 1b6ccf9: Identify authenticated CLI users to product analytics for better support and self-serve activation diagnostics.

## 0.95.0

### Minor Changes

- 3f963e8: Add a `momentic_test_get` MCP tool that returns a fully resolved test by id or path, including stable step ids and parent chains.

### Patch Changes

- 1d8a758: Do not fail the run when archiving artifacts is blocked by a transient file lock on Windows (OneDrive sync, antivirus).
- ec59187: Move the test output to respect your agents output to file or inline for mcp.
- e1daa0c: `consoleLogger` now writes `.error` and `.warn` output to stderr while `.info`, `.success`, `.debug`, and other variants continue writing to stdout, so `momentic run > out.log 2> err.log` cleanly separates progress from errors. `--log-level error` now silences `.success`, `.dimmed`, `.bold`, `.underline`, and `.grey` decorative variants as users expect.
- 4f2eb35: Improve schema validation performance and error messages
- 0e5015a: `momentic run` and `momentic-mobile run` now print a two-line summary banner at the top (CLI version, Node version, project, test count, shard). Per-test status badges fall back to plain ASCII `[PASS]` / `[FAIL]` on terminals without truecolor + unicode + TTY, and completed status rows no longer carry the running-progress counter.

## 0.94.0

### Minor Changes

- 2fcf445: Highlight where interactions happened for mobile runs

## 0.93.1

### Patch Changes

- c1e6c6f: `momentic app` and `momentic-mobile app` now show a clean startup banner with the local URL and version. Update-available notices are shown as a boxed message and skipped in CI / non-TTY shells. List commands (`momentic list`, `momentic-mobile list`, `momentic quarantine list`) are now safe to pipe — only test paths go to stdout. `momentic-mobile` now also checks for new releases on startup.
- 41bbc60: Fix run viewer video player flickering selected step back to its parent during gaps between substeps in a module or conditional.
- 9dbc7e0: Fix unexpected error when a directory being written to doesn't already exist.
- 45e126e: Fix Pylon chat support widget not appearing in the local app sidebar
- c1e6c6f: `momentic-mobile run` now prints the list of scheduled tests before the run starts. Wizard falls back to plain-text logging when stdout is not a TTY.
- 943797f: Fix zod4 external dependency issue

## 0.93.0

### Minor Changes

- b287497: Enable the mcp's splice and run step to work with setup and teardown sections for both iOS and Android tests.

### Patch Changes

- 0128aa9: Adding module parameter inputs should now show auto complete for each parameter option added

## 0.92.1

### Patch Changes

- a9355c9: Improve failure recovery for failures that happen inside a module in a test's setup or teardown steps — the recovery now considers the surrounding setup/teardown steps as context instead of just the failed module's inner steps.

## 0.92.0

### Minor Changes

- e2dbb11: Allow disabling of cache for relevant step types through the CLI and MCP

### Patch Changes

- 2a83857: Avoid CLI crash on startup when local diagnostics telemetry initialization fails

## 0.91.0

### Minor Changes

- 341994e: Editor supports drag and drop in and out of conditionals and modules

### Patch Changes

- d509349: Fix issue where resizing editor and run viewer stacked panels would trap element focus and prevent step keyboard navigation
- a1f29d3: Fix mobile editor not clearing the Target element field on a Type step

## 0.90.2

### Patch Changes

- f23b4e2: Fail fast with a clear error if connecting to a remote iOS or Android emulator stalls, instead of hanging the run indefinitely.

## 0.90.1

### Patch Changes

- 063d5c3: Improve step search relevance.
- e72d317: Add cmd/ctrl+z and cmd/ctrl+shift+z keyboard shortcuts for undo and redo in the mobile editor
- 11e7140: Fix "(intermediate value).env is not a function" crash on startup that could occur in some package manager layouts.

## 0.90.0

### Minor Changes

- 0a2767d: Extend MCP to support iOS module creation.

### Patch Changes

- 65418b2: Fix Android module steps so reusing the same module no longer overwrites earlier inputs, and require all non-defaulted parameters to be set when inserting a module.

## 0.89.2

### Patch Changes

- 9ce2e44: Local run viewer: left/right arrow keys now swap between before/after screenshots.
- d35564a: Slim down install size by removing unused dependencies.
- 61388c3: Redesign the run viewer header and details panel: the failure classification chip is now hover-only, the details panel defaults to closed, and browse vs. action buttons are visually separated.
- 068752d: Fix issue with relative position xy input labels causing values to be hidden
- f8a12dd: Only mark runs as recovered when the heal actually saved the run
- 61388c3: Fix JavaScript step type declarations so that the email.create() API shows up in editor autocomplete and type checking.
- 61388c3: Stop the CLI from crashing with broken-pipe and Sentry errors when its output is piped into commands like head or aborted mid-stream.
- 0f5a616: Fix issue where saving module tests with default parameters but no input value would cause validation error
- 2186f2d: Improve efficiency of git resolution for editor sessions, making the run button faster to begin executing steps.
- 61388c3: Make run viewer step rows keyboard-accessible: Tab moves focus through steps and Enter or Space selects a focused step.
- ad60d80: Patch critical security vulnerabilities in mobile testing dependencies.
- 85cf7c8: Fix issue with test editor inputs rejecting pasted text with new lines
- 61388c3: Tidy up run rows and tables: replace stacked badges with a single chip cluster for clearer status, classification, and label information.

## 0.89.1

### Patch Changes

- 21092a5: Fix issue with run viewer panels overflowing for some tests
- c6caa20: Display further details about conditional step configuration in run viewer
- 8f9463c: Fix issue where opening javascript editor in larger view would not correctly hydrate code
- 746430a: Fix AI ACTION v3 step incorrectly failing when no actions were needed to achieve its goal.

## 0.89.0

### Minor Changes

- 3d2f9b3: Added `email.create()` for provisioning fresh ephemeral email inboxes from inside a test at runtime. The returned inbox auto-expires after 24h.
- 55f156c: Added `sms.lease()` and `sms.release()` for checking a free number out of your org's pool for the duration of a test. See [SMS docs](https://docs.momentic.ai/integrations/sms#sms-lease-and-sms-release).
- 7560379: Update mobile editor and run viewer to use two panel layout
- 8c45334: Make the results path optional in `momentic results upload`, defaulting to the same `test-results` directory that `momentic run` writes to.

### Patch Changes

- eace3c1: Prevent apps from being closed when appium server is restarted
- 9de4134: Hide the `--api-key` default value in `--help` output so the CLI no longer prints the API key from `~/.momentic/auth.json`.
- 404e57a: Add absolute pixel coordinate targeting for the tap step
- eba24ff: Step tooltips on the video player timeline and resource usage charts now show "JavaScript" instead of the raw code for JavaScript steps, and the timeline tooltips dismiss when you move off the step rather than staying pinned open while hovering the tooltip itself.

## 0.88.2

### Patch Changes

- c9a69b0: Fix the self-hosted local results viewer (the static bundle shipped at
  `node_modules/momentic/run-viewer-static`) failing with "Unexpected
  Application Error! 404 Not Found" when opened directly via `index.html`.
  The viewer now once again shows the requested run whenever the URL
  includes a `?zipUrl=` query parameter.

## 0.88.1

### Patch Changes

- f9fb144: Run group timeline now anchors each run's bar at the run group's start time, so the "Waited for" segment is visible for CLI runs (which don't have a queuedAt). Wall time stat also stays accurate when the latest run finishes after the run group's recorded finishedAt.
- c358018: Improve reliability of usage telemetry.
- d50b82a: Clear the assertion's cache when failure recovery succeeds, so a recovered run no longer leaves a stale "false" memory trace that could cause future runs to incorrectly fail.
- b6f66b1: Address edge case caused by Chrome Dev Tools where some images would have no accessibility role, causing AI Assertion and locator inconsistencies

## 0.88.0

### Minor Changes

- 2ffb125: Fix Android cache resolving to the wrong element when a clickable container's visible label lives in a child view.

## 0.87.0

### Minor Changes

- d8fddb6: Improve AI action's ability to use and reason around SCROLL_TO steps and undo state changes after mistakes.

## 0.86.0

### Minor Changes

- ee94b03: Support adding files to iOS devices

### Patch Changes

- 701ddf7: Show the emulator region that was used in run results.
- 92c2ec5: Patch security vulnerabilities.
- 28338d8: Move iOS appium driver app installation to the client side.

## 0.85.2

### Patch Changes

- 2505fd1: Local results viewer (`cli results view` / `mobile-cli results view`) now
  renders per-attempt timeline segments for runs that retried. Previously the
  viewer showed a single bar per run regardless of how many attempts it took;
  now each attempt appears as its own colored segment with transparent gaps
  between attempts, matching the cloud run-group page.

## 0.85.1

### Patch Changes

- 5556ee3: Fix CLI sometimes hanging after a successful run.

## 0.85.0

### Minor Changes

- afc42a2: Add AUTO setting for parallelism for runs

### Patch Changes

- 4cf851c: Reduce CLI bundle size for faster installs.
- 81c9920: Patch transitive `axios` dependency to 1.15.2 to address a critical Prototype Pollution vulnerability ([CVE-2026-42264](https://security.snyk.io/vuln/SNYK-JS-AXIOS-16417750)).

## 0.84.1

### Patch Changes

- 583541d: Stream mobile asset uploads from disk instead of buffering the whole file in
  memory. This avoids OOMs on large builds.
- 610db75: Update Appium iOS and Android drivers to patch known security vulnerabilities

## 0.84.0

### Minor Changes

- d40190d: AI action V3 (alpha) is now the recommended version. The version dropdown is labeled "V3 (alpha)" in both the web and mobile editors, with help text explaining when to use V3 vs V2. V2 is described as the previous-generation fallback.

### Patch Changes

- 72ce2d6: Fixed lag when opening "View details" on the tests table.

## 0.83.1

### Patch Changes

- c5b52d1: Add in-app support chat widget to the local app.
- 4f9519e: The setup wizard now adds the sample environment(s) the scaffolded test depends on, even when a `momentic.config.yaml` already exists, so the very first run no longer fails with a missing-environment error. Mobile projects also get a sample environment so it's clear how to configure variables. Failures during the sample test, the editor-skills install, and the CLI install now show the full underlying output instead of being truncated to the last few lines. CLI command help, log messages, and READMEs now refer to the "Momentic dashboard" instead of "Momentic Cloud".

## 0.83.0

### Minor Changes

- a04408e: Support deleting uploaded mobile assets

### Patch Changes

- 2fc0994: Reduced redundant network requests from the local app frontend.
- a036c08: Speed up local app load times by caching filesystem operations
- c284376: Align init and upgrade configs with wizard defaults: add useMemory, failure recovery v2.0, and mobile upgrade command

## 0.82.0

### Minor Changes

- 2cb1630: Added support for local iOS emulators for the start session tool on the mobile mcp.
- 4dda8de: Add support for the --video flag in the mobile cli.
- 3de5629: Extend splice tool to support iOS in the mobile mcp.
- 293002f: Extend the run step tool to iOS emulators.
- c623608: Add support for preview step on iOS emulators

### Patch Changes

- 44011c1: Improve agent prompting for working with Momentic artifacts and their relative paths.
- d9f320b: Fix occasional crash in long Copilot sessions and improve long-context performance of agents.
- 5995687: Use the text attribute for text-based caching of native iOS elements
- 898231c: Fix the authoring guide on the start session to match the expected cli inputs of the mobile platform of the test.
- 1fb746c: Improve telemetry for test run completion events.

## 0.81.2

### Patch Changes

- 5351691: Display redacted env var values as "-" in the run viewer.
- d47df2a: Add available iOS simulator device types to the get artifacts tool output
- 6476fe4: Add drag handle for step settings card
- 433395f: When pressing enter for selecting a package, first package will be selected.

## 0.81.1

### Patch Changes

- 72320ea: iOS - AI actions now recover gracefully when the AI model returns without explicitly finishing the action.

## 0.81.0

### Minor Changes

- b230be2: Add support for iOS MCP start session tool using remote emulators.

### Patch Changes

- bf7acd8: AI actions now recover gracefully when the AI model returns without explicitly finishing the action.
- f4448f1: Patch transitive axios vulnerability (CVE-2026-42035, CVE-2026-42033).
- 230f2bc: Fix AI Action v2 not being able to clear input fields
- 930c9ee: Fix duplicated settings overlay

## 0.80.2

### Patch Changes

- fb6bdf0: Upgrade internal dependencies to fix known security vulnerabilities.
- cac4d74: Patch axios to 1.15.1 to fix critical HTTP Response Splitting and Prototype Pollution vulnerabilities.
- eec2918: Resolve iOS webview caches
- 559eb16: Cache git metadata fetches to improve app load performance
- 1c96b5b: Improve error response when trying to initialize multiple emulator sessions, so agents can recover without an extra retry.
- ee72ad5: MCP server now streams progress updates when `--daemon` is enabled, so long-running tools can report incremental status.

## 0.80.1

### Patch Changes

- c51b3f4: Generate caches for nodes inside webviews on iOS
- dc5b130: When --api-key falls back to ~/.momentic/auth.json, --server now also defaults to the server URL stored alongside that key, so a wizard login against staging no longer silently sends the staging key to the production server.
- dc5b130: - `momentic init` now writes only `momentic.config.yaml`; sample module and test scaffolding moved into the `@momentic/wizard` onboarding flow so manual installs stay minimal.
  - `momentic install-skills` and `momentic-mobile install-skills` are now deprecated. They still work, but prefer `npx skills@latest add momentic-ai/skills` — it auto-detects `.claude/`, `.cursor/`, `.agents/`, `.opencode/`, `.github/copilot/` and lets skill updates ship independently of the CLI.
  - The CLI now falls back to `~/.momentic/auth.json` (written by `momentic-wizard login`) when `MOMENTIC_API_KEY` isn't set.

## 0.80.0

### Minor Changes

- 5ed5ab4: Increase maximum individual session duration for websocket-based clients like classification and AI action to 5 minutes

## 0.79.3

### Patch Changes

- ac9df82: Filter out noisy "Creating hash file directory" lines from Appium logs
- ebf509c: Show intellisense for env variables in the Monaco editor based on the current test context

## 0.79.2

### Patch Changes

- 2c77f29: Improve reliability of AI agent streaming responses while preserving reasoning context where possible.
- b3f95b9: Remove unnecessary error logs from the console
- b3f95b9: Ensure emulators are properly cleaned up after cancelled runs

## 0.79.1

### Patch Changes

- 91253d2: Enable waiting for stability by default for iOS
- 5bdd51e: Fix edge case where Momentic would give up on scrolling too early for text-only dropdowns
- 91253d2: Optimize speed of fetching iOS accessibility tree

## 0.79.0

### Minor Changes

- cb6678b: Add `assets list` command to list asset channels and tags grouped by platform.

### Patch Changes

- 083ee13: Display iOS syslogs in the mobile editor
- 2e86c07: Add intellisense to the javascript editor
- 534e1f8: Upgrade appium dependencies to address security vulnerabilities
- 6c82d84: Add the ability to pop out the Javascript editor into a larger window
- 083ee13: Collect syslog logs during iOS test runs

## 0.78.0

### Minor Changes

- 6fcfc99: Improve Android locator prompts and model performance

## 0.77.3

### Patch Changes

- 10dc30c: Try to restart appium connection if there are too many failures

## 0.77.2

### Patch Changes

- 4313b4f: Show AI Action version in run viewer

## 0.77.1

### Patch Changes

- cc4fcbd: Fix a bug where tests were not shown in the local app UI on Windows

## 0.77.0

### Minor Changes

- ce25160: MCP: Consolidate session and step schema retrieval into the session start tool. Updated the `momentic-test` skill to match.

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

- b22cce8: Improve template string syntax highlighting in step editor form inputs
- a41dea2: Report emulator region on new run results in the run viewer details pane.
- 4f24aea: Make editor floating step card draggable
- ef7f299: Change conditionals to show the status of the conditional not the conditional and substeps.

## 0.73.2

### Patch Changes

- 1d986d8: Improve reliability of AI response streaming.

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
- 243d779: Loosen timeouts for screenshots and page source on slower emulator providers
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

- 66862b0: Ship skill markdown as separate file assets under `skills/` for easier inspection.
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
- 8d41b69: Mobile MCP now defaults to the test's emulator settings, then remote emulators, and only uses local emulators when explicitly requested.
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
- 5fa34ba: Tune tool descriptions to encourage better agent behavior when editing.

## 0.54.0

### Minor Changes

- 893e28a: Removed the momentic_module_list tool from the mcp and moved its functionality to the get attributes tool.
- 893e28a: Renamed the momentic_attributes_list to momentic_get_attributes.

### Patch Changes

- 893e28a: Improved the error handling and description of the get attributes tool.
- 893e28a: Improved the momentic-test skill to better understand the get attributes tool.

## 0.53.1

### Patch Changes

- a5c98fc: Mobile MCP `get attributes` tool now returns `availableChannels` for agents to use when creating tests.

## 0.53.0

### Minor Changes

- 4a3c90f: Add the preview step tool to the momentic mobile mcp.
- b850fcf: Add the get initial data tool for mobile mcp.
- fe5c302: Add the splice tool to the momentic mobile mcp server.

### Patch Changes

- 889afe5: Update run viewer details panel styles
- de63f5c: Improve response message to the model when cache entries fail to save inside the mcp's splice tool.
- e749e10: Sentence case step type names (AI check, Element check, Page check) across UI labels, error messages, and agent prompts
- d8d300e: MCP step inputs now use `*-fraction` instead of `*-percentage` for clarity.

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

- da6baed: Display the actual connected emulator region in the mobile editor device preview
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

- 049e435: Fix Open App packages input requiring two clicks to type

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
- ce4dd29: Fix soft reset killing internal test driver apps on iOS

## 0.47.0

### Minor Changes

- 1098b96: Enable iOS AI action support

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
- 45b4d64: Add iterations and tap delay support to iOS tap steps

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

- 43e9d4d: Improve internal logging for mobile step cache eviction

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

- 74fd5f5: Fix internal editor state bug
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

- ee96a70: Preserve test execution status and traces when data refreshes in the background

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

- 9fdae76: Fix issue with handling numerical values in DOM processing

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
