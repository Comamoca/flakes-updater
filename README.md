<div align="center">

![Last commit](https://img.shields.io/github/last-commit/Comamoca/update-flakes?style=flat-square)
![Repository Stars](https://img.shields.io/github/stars/Comamoca/update-flakes?style=flat-square)
![Issues](https://img.shields.io/github/issues/Comamoca/update-flakes?style=flat-square)
![Open Issues](https://img.shields.io/github/issues-raw/Comamoca/update-flakes?style=flat-square)
![Bug Issues](https://img.shields.io/github/issues/Comamoca/update-flakes/bug?style=flat-square)

<img src="https://emoji2svg.deno.dev/api/🦊" alt="eyecatch" height="100">

# flakes-updator

Automatically updates all Nix flake.lock files in your repository and creates a pull request with the updates.

<br>
<br>


</div>

<div align="center">

</div>

## 🚀 How to use

```yaml
- name: Update Nix Flakes
  uses: comamoca/update-flakes@v1
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```

## ⬇️  Install

This is a GitHub Action. Add it to your workflow file:

```yaml
name: Update Flakes
on:
  schedule:
    - cron: '0 0 * * 0'  # Weekly on Sunday
  workflow_dispatch:

jobs:
  update-flakes:
    runs-on: ubuntu-latest
    steps:
      - uses: comamoca/update-flakes@v1
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```


## ⛏️   Development

```sh
# Clone the repository
git clone https://github.com/Comamoca/update-flakes
cd update-flakes

# Test the action locally
act -j update-flakes
```
## 📝 Features

- [x] Automatically finds all flake.nix files in repository
- [x] Updates flake.lock files with nix flake update
- [x] Creates pull request with updated dependencies
- [x] Customizable commit messages and PR titles

## 📜 License

MIT License

### 🧩 Requirements

- GitHub Actions environment
- Nix with flakes enabled
- Repository with flake.nix files

## 👏 Inspired by

This action helps maintain up-to-date Nix dependencies automatically.

## 💕 Special Thanks

- [Nix](https://nixos.org/) for the amazing package manager
- [GitHub Actions](https://github.com/features/actions) for CI/CD platform
- [peter-evans/create-pull-request](https://github.com/peter-evans/create-pull-request) for PR creation
