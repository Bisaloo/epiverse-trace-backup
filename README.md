<!-- badges: start -->
[![Automation
status](https://github.com/epiverse-trace-bot/epiverse-trace-backup/workflows/backup-and-upload/badge.svg)](https://github.com/epiverse-trace-bot/epiverse-trace-backup/actions)
<!-- badges: end -->

This repository contains the automation code for weekly backups of the [`Epiverse-TRACE`](https://github.com/epiverse-trace) and [`Epiverse-CONNECT`](https://github.com/epiverse-connect) GitHub organisation.

This is achieved by [replicating the back-up infrastructure from rOpenSci](https://discuss.ropensci.org/t/backing-up-github-organisation-with-gitcellar/3153) documented in the ["Safeguards and Backups for GitHub Organizations" blog post](https://ropensci.org/blog/2022/03/22/safeguards-and-backups-for-github-organizations/).

Migration archives are created with [gitcellar](https://docs.ropensci.org/gitcellar/) and are then uploaded to a [Google Cloud Platform](https://console.cloud.google.com/) storage bucket.

This is automated via GitHub Actions and runs on a weekly basis (each Saturday in the night).

For increased security, this repo is hosted on a dedicated GitHub account, @epiverse-trace-bot, which also provides a Personal Access Token (PAT) with minimal permissions.
