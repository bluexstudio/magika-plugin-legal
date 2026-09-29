# Diff Notes Documentation

Diff Notes captures private review notes from normal code editors and native
text diff views. It keeps notes local to the current JetBrains project and can
copy a Markdown report when the reviewer is ready.

## Getting started

1. Install Diff Notes and open a local project.
2. In a normal editor or native text diff, place the caret on the line you want
   to review.
3. Right-click and choose **Add Private Review Note**.
4. Enter the note and confirm it.
5. Open **View > Tool Windows > Diff Notes** to review saved notes.
6. Select a note and choose **Open** to return to its location, or choose
   **Copy Markdown** to copy a grouped report.

## How line relocation works

Diff Notes stores the exact target line plus its immediate neighboring context.
When lines are inserted above the target, that context can relocate the note.
If the target itself changed and no exact contextual match remains, Diff Notes
falls back to the original stored line instead of making a weak guess. Always
verify the location before sharing review feedback.

## Storage and privacy

Notes are stored in IntelliJ's local project workspace state, which can include
`.idea/workspace.xml`. Keep workspace state untracked when notes must remain
private. The plugin does not edit source files, create repository files, post
to GitHub or GitLab, collect telemetry, or use a network or account.

Diff Notes is not a backup service. Copy important reports to durable storage.

## Limits

A project stores up to 500 notes. Each note can contain up to 2,000 characters.
These limits keep local report generation predictable.

## Privacy and support

- [Privacy notice](Diff-Notes-PRIVACY.md)
- [End-user license agreement](Diff-Notes-EULA.md)
- [Support](SUPPORT.md)

