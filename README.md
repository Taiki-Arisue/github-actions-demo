# GitHub Actions Demo

This repository demonstrates a minimal Go project wired with GitHub Actions to run tests on every push and pull request.

## Project structure

- `main.go`: Simple entry point that prints a greeting
- `main_test.go`: Minimal unit test
- `.github/workflows/`: Place for CI workflows (add your own if needed)

## Requirements

- Go 1.21+
- GitHub Actions (enabled in this repository)

## Local development

```bash
# Run tests
go test ./...

# Run the app
go run .
```

## Continuous Integration (CI)

Below is an example workflow you can add at `.github/workflows/ci.yml`:

```yaml
name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-go@v5
        with:
          go-version: '1.21.x'
      - run: go version
      - run: go test ./...
```

## How to use

1. Open a pull request to trigger CI on PRs.
2. Push to `main` to trigger CI on direct pushes.
3. Extend workflows as needed (linting, build, release).

## License

MIT