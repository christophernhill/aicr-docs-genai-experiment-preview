# Agent Instructions -- previews repository

This is the **previews repository** in the three-repository MkDocs documentation
architecture. It hosts temporary per-PR preview deployments.

## Purpose

When a PR is opened in the edit repository, CI builds the docs and pushes the output
to a `pr-<N>` branch in this repository. GitHub Pages serves each branch as a preview.

## Contents

- `.nojekyll` -- Disables Jekyll processing
- `README.md` -- Repository description

All other content is pushed by CI workflows from the edit repository. Each PR gets
its own branch (`pr-1`, `pr-2`, etc.) containing a full built MkDocs site.

## GitHub Pages configuration

- Build and deployment: **GitHub Actions** (not "deploy from branch")
- This is required for branch-per-PR to work -- each new branch triggers its own
  Pages deployment

## Preview URL pattern

```
https://christophernhill.github.io/-previews/pr-<N>
```
