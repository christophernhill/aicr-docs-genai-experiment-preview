# -previews

PR preview repository for the AICR Documentation - Gen AI experimenting documentation site.

When a pull request is opened in the
[`christophernhill/-edit`](https://github.com/christophernhill/-edit)
repository, a CI workflow builds the documentation and pushes the result to a
`pr-<N>` branch in this repository. The preview is then available at:

```
https://christophernhill.github.io/-previews/pr-<N>
```

**Do not edit files in this repository directly.** All content is deployed
automatically by CI.

## GitHub Pages

This repository must have GitHub Pages configured to deploy from **GitHub Actions
workflow** (not a static branch). This is required for the branch-per-PR preview
strategy to work.

To configure: repository settings > **Pages** > Build and deployment > **GitHub Actions**.
