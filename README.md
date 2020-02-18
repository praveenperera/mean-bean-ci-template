# 🦀 Ferris' Mean Bean CI Machine

This is a template for GitHub Actions meant as a successor to [`japaric/trust`](https://github.com.japaric/trust)
for handling [`XAMPPRocky/tokei`](https://github.com/XAMPPRocky/tokei)'s CI and
deployment. I decided to make it a template to be able share it across
projects and with the community.

## Features

- ⚒️ **Test Everywhere.** Build & Test your Rust project up to **50**
  different targets with three different release channels.
- 🙅‍♀️ **No Configuration.** Set your binary name and you're good to go!
- 🚁 **Automatic GitHub Deployments.** Build binaries for any tagged release.
- 🏭 **Massively Parallel.** Each job is run in parallel, the only limit is your GitHub
  plan.

## Using this template

There are two main CI files in this template.

- [`mean_bean_ci.yml`](./.github/workflows/mean_bean_ci.yml) — Handles push & pull request build and testing.
- [`mean_bean_deploy.yml`](./.github/workflows/mean_bean_deploy.yml) — Handles deploying to GitHub Releases on tag push. Delete this if don't want any deployments.

The only thing you need to change to make this template work is update the `BIN`
environment variable to the name of your binary, and you're good to go!

## Customising Build & Test
You can customise the build and testing in [`ci/build.bash`](./ci/build.bash) and [`ci/test.bash`](./ci/test.bash)
respectively.
