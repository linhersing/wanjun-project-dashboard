# H-wide Explorer Acceptance Gallery - 2026-07-05

This private-repo gallery records GitHub-safe acceptance evidence for the H experimental wide file explorer.

- Branch: `feature/dynamic-index-preview-poc`
- Commit: branch HEAD after this change; see Codex final report for the immutable SHA.
- Version: `v2026.07.01-18`
- Scope: H experimental drive only
- Entry: `/__wanjun/h-explorer`
- Mechanical validation: `PASS 46 / FAIL 0 / PENDING_MANUAL 3 / NOT_IN_SCOPE 0`
- Office real-window launch: `PENDING_MANUAL`

Safety notes:

- F drive was not touched.
- `main` was not merged.
- Version was not bumped.
- Official root BAT was not modified.
- No F/H source-data sync was performed.
- No permanent delete was performed; delete operations moved test data to the H safe recycle area.
- SQLite, logs, runtime, temp outputs, secrets, real driveId, and local reports are not committed.

The images in `assets/` are GitHub-safe visual evidence generated from the H explorer API and validation report. They use stable relative paths and mask or omit local absolute paths and driveId.

## Screenshots / Evidence

1. `01-h-root-main-folders.png` - H root main folders are visible, with protected system area marked.
2. `02-enter-normal-folder.png` - Entered an H normal data folder.
3. `03-parent-navigation.png` - Parent navigation metadata is available.
4. `04-windows-open-folder.png` - Windows open contract for an H sandbox folder.
5. `05-created-folder.png` - New folder appears after create operation.
6. `06-renamed-file.png` - Renamed Office file appears and old name is removed.
7. `07-copy-paste-result.png` - Copy/paste result appears in destination folder.
8. `08-cut-move-result.png` - Cut/move result appears in destination folder.
9. `09-search-updated.png` - Search result reflects SQLite/page update.
10. `10-protected-area-blocked.png` - Protected system area mutation is blocked.
11. `11-test-report-summary.png` - Mechanical validation summary.
