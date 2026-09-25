# FlagScope Documentation

FlagScope finds and audits feature-flag definitions and usages inside the current JetBrains IDE project. Analysis is local and read-only: project source code is not uploaded, telemetry is not collected, and project files are not modified.

## Getting started

1. Install FlagScope from JetBrains Marketplace and open a project.
2. Open **View > Tool Windows > FlagScope**, or choose **Tools > Scan Feature Flags**.
3. Wait for the background scan to finish. Cancelling a scan keeps the most recent completed results.
4. Search or filter the results, select a flag, then open a definition or usage by double-clicking it or pressing **Enter** or **F4**.

## Free features

- Background scanning with safe cancellation.
- Search and status filters for detected, possibly unused, definition-only, and unresolved flags.
- Definition and usage counts with the matching convention shown for each location.
- Navigation from a result to the corresponding local source location.

## FlagScope Pro

- Company-specific qualified call names and custom YAML or JSON section names.
- Additional built-in recognition for Statsig, Flipt, GrowthBook, Firebase Remote Config, and Optimizely styles.
- Audit priorities, findings, suggested next steps, and duplicate-definition guidance.
- Local baselines comparing added, removed, and status-changed flags.
- Local Markdown, CSV, and JSON audit reports with an executive summary and detected conventions.

Use **Pro Rules** to configure organization-specific conventions, **Baseline Pro** to compare the current scan with a saved local baseline, and **Export Pro** to create a local audit report.

## Supported files and conventions

FlagScope scans Java, Kotlin, JavaScript, JSX, TypeScript, TSX, JSON, YAML, and YML files. Detection is based on documented local conventions and does not claim to determine a feature flag's runtime state.

Files over 2 MB and unreadable files are skipped to protect IDE responsiveness. The scan summary reports skipped files so partial results are visible.

## Troubleshooting

- **No results:** confirm the project contains supported files and use **Tools > Scan Feature Flags** to start a new scan.
- **Partial scan:** review the skipped-file counts shown in the status area.
- **Possible stale:** treat this as a review signal, not proof that a flag is unused. FlagScope found a definition but no matching usage under its supported conventions.
- **Navigation does not open a location:** rescan after files or project roots change.

## Privacy and support

- [Privacy notice](FLAGScope-PRIVACY.md)
- [End-user license agreement](FLAGScope-EULA.md)
- [Support](SUPPORT.md)
