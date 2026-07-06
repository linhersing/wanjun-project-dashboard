# H Explorer Acceptance Gallery - 2026-07-05

This private-repository gallery records GitHub-safe acceptance evidence for the H experiment file browser.

## Scope

- Branch: `feature/dynamic-index-preview-poc`
- Base checkpoint before this gallery: `8a5f478`
- Program version: `v2026.07.01-18` (unchanged)
- Entry under test: `/__wanjun/h-explorer`
- Test data: H temp mirror plus two small real H roots in read-only mode
- Not included: SQLite, logs, runtime, temp fixtures, full local paths, true driveId, secrets, raw F/H data

## Result Summary

| Area | PASS | FAIL | PENDING_MANUAL | NOT_IN_SCOPE |
| --- | ---: | ---: | ---: | ---: |
| H temp mirror operation regression | 38 | 0 | 3 | 0 |
| Real H root read-only: annual media | 11 | 0 | 0 | 0 |
| Real H root read-only: guest coffee | 10 | 0 | 1 | 0 |
| Future F/replica rollout | 0 | 0 | 0 | 1 |
| Total | 59 | 0 | 4 | 1 |

Office actual window launch remains `PENDING_MANUAL`: Word, Excel, and PowerPoint are mechanically verified with stable relative path, resolved path, existence, and `windows-default-file` dryRun mode, but real app windows still require Tuesday manual acceptance.

## Screenshots

Open each image directly to zoom.

1. [H explorer home](assets/01-h-explorer-home.png)
2. [Toolbar and search](assets/02-toolbar.png)
3. [Row action buttons](assets/03-row-actions.png)
4. [After create folder](assets/04-after-create-folder.png)
5. [After rename](assets/05-after-rename.png)
6. [After copy/paste](assets/06-after-copy-paste.png)
7. [After cut/move](assets/07-after-cut-move.png)
8. [After move to experiment recycle](assets/08-after-recycle.png)
9. [Open validation record](assets/09-open-validation-record.png)
10. [Test report summary](assets/10-test-report-summary.png)

## GitHub-Safe Checks

- Screenshots show only the H temp mirror UI or sanitized report sections.
- Screenshots do not show a true driveId, full local path, secrets, or private raw documents.
- Operation logs and complete JSON reports remain on the H temp area only.
- No F drive check, mutation, or sync was performed.

## Local Evidence Not Committed

- Full operation report: `<H_TEMP_MIRROR>/reports/h-explorer-ops-full.json`
- Operation log: `<H_TEMP_MIRROR>/logs/h-explorer-operations.jsonl`
- Experiment recycle: `<H_TEMP_MIRROR>/experiment-recycle`

