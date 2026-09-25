# Changelog Pilot Documentation

Changelog Pilot converts a bounded local Git commit range into grouped, reviewable Markdown. It reads local Git history without publishing releases, creating tags, changing commits, or modifying repository files.

## Getting started

1. Install Changelog Pilot from JetBrains Marketplace and open a Git project.
2. Open **View > Tool Windows > Changelog Pilot**, or choose **Tools > Open Changelog Pilot**.
3. Enter a local ref such as `HEAD`, or a bounded range such as `v1.0.0..HEAD`.
4. Generate the changelog and review the Markdown preview.
5. Use the copy action to place the reviewed Markdown on the clipboard.

## Features

- Local Git ref and `base..head` range support.
- A 500-commit safety cap and 15-second process limit.
- Grouping by common Conventional Commit type and scope.
- A dedicated breaking-change section.
- Escaped, reviewable Markdown preview and copy action.
- No network access, AI, account, telemetry, release publishing, or repository writes.

Commits that do not follow Conventional Commits are retained under **Other**.

## Troubleshooting

- **No output:** confirm the open project has a local Git repository and the requested ref or range exists.
- **Invalid range:** use a local ref such as `HEAD`, or a range in `base..head` form.
- **Large history:** select a narrower range; Changelog Pilot reads at most 500 commits per request.
- **Git timeout:** retry with a smaller range and confirm the local Git executable is responsive.

## Privacy and support

- [Privacy notice](Changelog-Pilot-PRIVACY.md)
- [End-user license agreement](Changelog-Pilot-EULA.md)
- [Support](SUPPORT.md)
