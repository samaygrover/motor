
## Branching workflow (project-wide standard, 2026-05-07)

This repo follows: **`claude/<feature>` → `develop` → `main`**

Rules:
1. ALWAYS branch off `develop`, not `main`: `git checkout -b claude/<task> develop`
2. ALWAYS target `develop` when opening PRs: `gh pr create --base develop`
3. NEVER push directly to `main` or `develop` (both protected; pushes will fail)
4. Squash-merge by default
5. Keep PRs small (one feature/fix per PR; > 25 files → split)
6. Verify PR scope before merging — file count should match expectation

`develop` and `main` are auto-synced by `.github/workflows/sync-develop-from-main.yml` after every merge to `main`. Don't try to sync manually.

Full operating guide: `automation-projects/docs/CLAUDE_GITHUB_SETUP.md`