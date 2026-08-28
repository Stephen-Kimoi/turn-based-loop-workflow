# Test A UI Feature With Evidence-Driven Testing

Replace `<FEATURE_DESCRIPTION>`, `<APP_URL>`, and `<TEST_ENVIRONMENT>` before using this prompt.

```text
Test this user-interface feature using the AI Software Delivery Workflow's evidence-driven testing
reference:

<FEATURE_DESCRIPTION>

Application URL or launch target:
<APP_URL>

Environment:
<TEST_ENVIRONMENT>

Use the workflow from:
https://github.com/Stephen-Kimoi/ai-software-delivery-workflow

Specifically follow:
https://github.com/Stephen-Kimoi/ai-software-delivery-workflow/blob/main/references/evidence-driven-testing.md

This is an independent UI verification task. Do not modify the implementation, change test data
outside the intended flow, push changes, merge a PR, or claim success for evidence that was not
captured.

1. Establish the exact version under test. Record the repository, branch, commit SHA or deployed
   build, local or deployed URL, browser and version, operating system, viewport, and relevant
   feature flags or environment settings. Start from the authenticated or unauthenticated state
   required by the test unless setup itself is under test.
2. Read the feature description, acceptance criteria, relevant implementation and automated tests,
   and any repository instructions. Build a verification matrix mapping every required behavior to
   its expected result, UI interaction, automated coverage, and evidence status.
3. Prepare a maximized, uncluttered browser or application window. Close unrelated popups,
   notifications, and panels. Mask credentials, tokens, cookies, personal data, and secrets.
4. Start recording before the first meaningful action. Add a setup annotation that states the
   starting context, test data assumptions, and environment.
5. Test the complete real user flow, not an isolated happy-path click. Add short plain-language
   `test_start` annotations for each behavior under test. After each meaningful state change, add
   a short `assertion` annotation marked `passed`, `failed`, or `untested`.
6. Cover the applicable scenarios: initial and resulting UI state, successful flow, validation and
   malformed input, empty/loading/error states, boundaries, duplicate submissions, retry or
   refresh behavior, navigation and persistence, permissions or unauthenticated access,
   responsive layout, keyboard access, and relevant browser or device differences. Do not invent
   scenarios that are outside the feature's acceptance criteria; explain why an applicable case is
   untested when prerequisites are unavailable.
7. Run the repository's relevant automated checks for real, including formatting, linting, type
   checks, unit tests, integration or end-to-end tests, and accessibility checks when available.
   Report each command, exit code, and meaningful result. A zero-test run is not a pass, and
   recorded UI evidence does not replace executable verification.
8. Stop and review the recording. Confirm that the setup, meaningful actions, resulting states,
   annotations, and assertions are visible and readable. Re-record if key evidence is missing,
   tiled, obscured, or covered by unrelated UI. If video recording is unavailable, capture
   screenshots and explicitly report that limitation.
9. Report the exact commit or deployment, browser, environment, viewport, test data limitations,
   and evidence paths or links. If reporting on a GitHub PR, include an inline-viewable GIF using
   an absolute raw commit URL and provide the full-quality MP4 path separately when possible.

Return:
- overall verdict: passed, failed, or blocked
- verification matrix for every required behavior
- scenario-by-scenario assertion results
- commands executed, exit codes, and real results
- browser, environment, version, viewport, and feature-flag details
- evidence paths or links, including the recording and GIF when available
- findings ordered by severity with exact file or UI references
- accessibility, responsive-layout, security, privacy, and data-integrity concerns
- untested behavior and exact blockers
- a final statement saying whether the feature is genuinely verified

Do not claim the UI works from memory or from source inspection. Acceptance requires the expected
behavior, automated checks, and recorded UI evidence to agree.
```
