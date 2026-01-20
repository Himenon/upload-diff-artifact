# upload-diff-artifact

A GitHub Action to upload build artifacts to GitHub Actions Artifacts at a specified path.
Use in conjunction with [Himenon/diff-artifacts](https://github.com/Himenon/diff-artifacts).

## Usage

**Single Target:**

```yaml
on:
  push:
    branches: [main]

jobs:
  upload:
    runs-on: ubuntu-latest
    steps:
      # build steps ...
      - uses: Himenon/upload-diff-artifact@v1.0.0
        with:
          path: dist/
```

**Multi Target:**

```yaml
on:
  push:
    branches: [main]

jobs:
  upload:
    runs-on: ubuntu-latest
    steps:
      # build steps ...
      - uses: Himenon/upload-diff-artifact@v1.0.0
        with:
          path: |
            apps/web/dist
            apps/api/dist
```

## Related

- [Himenon/diff-artifacts](https://github.com/Himenon/diff-artifacts)
- [Himenon/close-diff-artifact-pr](https://github.com/Himenon/close-diff-artifact-pr)

## License

[Himenon/upload-diff-artifact](https://github.com/Himenon/upload-diff-artifact), MIT
