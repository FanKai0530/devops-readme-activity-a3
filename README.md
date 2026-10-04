# Repository Activity Demo

This repository shows a scheduled GitHub Actions workflow that publishes recent commits to this README.

## Recent activity

<!-- activity:start -->
- 2026-10-05 · [Merge pull request #2 from FanKai0530/1-automate-recent-activity-in-readme](https://github.com/FanKai0530/devops-readme-activity-a3/commit/8fea6e8aa1771934ff33a1c345988c65fd6eeb52) (`8fea6e8`)
- 2026-10-05 · [ci: use current checkout action runtime](https://github.com/FanKai0530/devops-readme-activity-a3/commit/440de9736efbb27060f729af6ea397898aef9860) (`440de97`)
- 2026-10-05 · [feat: automate README activity and validate PR previews](https://github.com/FanKai0530/devops-readme-activity-a3/commit/f7ac76dcd06faca02656e3be355e36d881778303) (`f7ac76d`)
- 2026-10-05 · [docs: add README activity markers](https://github.com/FanKai0530/devops-readme-activity-a3/commit/a230650dfb683a5e60b4c9f36af588fb026429ec) (`a230650`)
<!-- activity:end -->

## How it works

The [update workflow](.github/workflows/update-readme.yml) runs daily or on demand. It reads recent commits, replaces only the marked section, and commits a change only when the section differs. The [validation workflow](.github/workflows/validate-readme.yml) checks the markers and updater on pull requests.

## Setup

1. Create a fine-grained personal access token limited to this repository, with **Contents: read and write**. The repository owner should do this in GitHub's token settings.
2. Save it as an Actions repository secret named `REPO_TOKEN`. Never put its value in a file, issue, slide, or log.
3. Run **Actions → Update README activity → Run workflow** once, then check the resulting README commit and workflow run.

The scheduled workflow uses the repository's default branch. GitHub may delay scheduled runs; the manual trigger is useful for demonstrations.
