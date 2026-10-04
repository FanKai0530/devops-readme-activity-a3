# Repository Activity Demo

This repository shows a scheduled GitHub Actions workflow that publishes recent commits to this README.

## Recent activity

<!-- activity:start -->
_The first workflow run will add recent commits here._
<!-- activity:end -->

## How it works

The [update workflow](.github/workflows/update-readme.yml) runs daily or on demand. It reads recent commits, replaces only the marked section, and commits a change only when the section differs. The [validation workflow](.github/workflows/validate-readme.yml) checks the markers and updater on pull requests.

## Setup

1. Create a fine-grained personal access token limited to this repository, with **Contents: read and write**. The repository owner should do this in GitHub's token settings.
2. Save it as an Actions repository secret named `REPO_TOKEN`. Never put its value in a file, issue, slide, or log.
3. Run **Actions → Update README activity → Run workflow** once, then check the resulting README commit and workflow run.

The scheduled workflow uses the repository's default branch. GitHub may delay scheduled runs; the manual trigger is useful for demonstrations.
