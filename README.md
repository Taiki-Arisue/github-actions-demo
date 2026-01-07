# 🚀 GitHub Actions Demo

[![CI](https://github.com/Taiki-Arisue/github-actions-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/Taiki-Arisue/github-actions-demo/actions/workflows/ci.yml)
[![CD](https://github.com/Taiki-Arisue/github-actions-demo/actions/workflows/cd.yml/badge.svg)](https://github.com/Taiki-Arisue/github-actions-demo/actions/workflows/cd.yml)
[![Go Version](https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat&logo=go)](https://golang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive demonstration repository showcasing **GitHub Actions CI/CD workflows** with a simple Go application. This project serves as a practical example for learning GitHub Actions, automated testing, and continuous deployment practices.

## 📋 Table of Contents

- [🎯 Project Overview](#-project-overview)
- [🏗️ Project Structure](#️-project-structure)
- [⚙️ Prerequisites](#️-prerequisites)
- [🚀 Quick Start](#-quick-start)
- [🔧 Local Development](#-local-development)
- [🔄 CI/CD Workflows](#-cicd-workflows)
- [📚 Learning Objectives](#-learning-objectives)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## 🎯 Project Overview

This repository demonstrates a complete **CI/CD pipeline** using GitHub Actions with a minimal Go application. It showcases:

- ✅ **Continuous Integration (CI)** - Automated testing on every push and PR
- ✅ **Continuous Deployment (CD)** - Automated deployment workflows
- ✅ **Go application** with unit tests
- ✅ **GitHub Actions workflows** with best practices
- ✅ **Multi-platform support** (Linux, macOS, Windows)

Perfect for developers learning GitHub Actions, DevOps practices, or looking for a template to start their own Go projects with CI/CD.

## 🏗️ Project Structure

```
github-actions-demo/
├── .github/
│   └── workflows/
│       ├── ci.yml          # Continuous Integration workflow
│       └── cd.yml          # Continuous Deployment workflow
├── main.go                 # Simple Go application
├── main_test.go           # Unit tests
├── go.mod                 # Go module definition
├── go.sum                 # Go module checksums
└── README.md              # This file
```

### Key Files

- **`main.go`**: Simple Go application that prints a greeting message
- **`main_test.go`**: Unit tests using Go's built-in testing framework
- **`.github/workflows/ci.yml`**: CI workflow that runs tests on every push/PR
- **`.github/workflows/cd.yml`**: CD workflow for automated deployments

## ⚙️ Prerequisites

- **Go 1.21+** - [Download here](https://golang.org/dl/)
- **Git** - [Download here](https://git-scm.com/downloads)
- **GitHub account** - [Sign up here](https://github.com/)

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/Taiki-Arisue/github-actions-demo.git
   cd github-actions-demo
   ```

2. **Run the application**
   ```bash
   go run main.go
   ```

3. **Run tests**
   ```bash
   go test ./...
   ```

4. **Fork and experiment** with the GitHub Actions workflows!

## 🔧 Local Development

### Running Tests

```bash
# Run all tests
go test ./...

# Run tests with verbose output
go test -v ./...

# Run tests with coverage
go test -cover ./...
```

### Building the Application

```bash
# Build for current platform
go build -o github-actions-demo .

# Build for specific platforms
GOOS=linux GOARCH=amd64 go build -o github-actions-demo-linux .
GOOS=windows GOARCH=amd64 go build -o github-actions-demo.exe .
GOOS=darwin GOARCH=amd64 go build -o github-actions-demo-macos .
```

### Code Quality

```bash
# Format code
go fmt ./...

# Run linter (if you have golangci-lint installed)
golangci-lint run
```

## 🔄 CI/CD Workflows

This repository includes two GitHub Actions workflows:

### 1. Continuous Integration (CI) - `ci.yml`

**Triggers:**
- Push to `main` branch
- Pull requests to `main` branch

**Features:**
- ✅ Multi-platform testing (Ubuntu, macOS, Windows)
- ✅ Go 1.21.x setup
- ✅ Automated test execution
- ✅ Go version verification

**Workflow Steps:**
1. Checkout code
2. Set up Go environment
3. Verify Go installation
4. Run tests across all platforms

### 2. Continuous Deployment (CD) - `cd.yml`

**Triggers:**
- Push to `main` branch (after CI passes)
- Manual workflow dispatch

**Features:**
- ✅ Deployment automation
- ✅ Environment-specific configurations
- ✅ Build artifacts management
- ✅ Notification integration

**Workflow Steps:**
1. Checkout code
2. Set up Go environment
3. Build application
4. Deploy to target environment
5. Send deployment notifications

### Workflow Status

You can view the current status of all workflows in the [Actions tab](https://github.com/Taiki-Arisue/github-actions-demo/actions).

## 📚 Learning Objectives

By exploring this repository, you'll learn:

### GitHub Actions Fundamentals
- How to create and configure workflow files
- Understanding triggers, jobs, and steps
- Working with different operating systems
- Using actions from the GitHub Marketplace

### Go Development
- Basic Go project structure
- Writing and running unit tests
- Go module management

### DevOps Best Practices
- Continuous Integration principles
- Automated testing strategies
- Deployment automation

### Advanced Topics
- Matrix builds for multiple platforms
- Conditional workflow execution
- Artifact management

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### 🐛 Reporting Issues

1. Check existing [issues](https://github.com/Taiki-Arisue/github-actions-demo/issues)
2. Create a new issue with:
   - Clear description
   - Steps to reproduce
   - Expected vs actual behavior
   - Environment details

### 🔧 Making Changes

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**
4. **Add tests** for new functionality
5. **Run tests locally**
   ```bash
   go test ./...
   ```
6. **Commit your changes**
   ```bash
   git commit -m "feat: add your feature description"
   ```
7. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```
8. **Create a Pull Request**

### 📝 Pull Request Guidelines

- Use clear, descriptive commit messages
- Include tests for new features
- Update documentation as needed
- Ensure all tests pass
- Follow the existing code style

### 🎯 Suggested Improvements

- Add more comprehensive tests
- Implement additional GitHub Actions features
- Add code coverage reporting
- Include security scanning
- Add performance benchmarks
- Create deployment documentation

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

[🔗 GitHub Actions Documentation](https://docs.github.com/en/actions) • 
[🔗 Go Documentation](https://golang.org/doc/) • 
[🔗 MIT License](https://opensource.org/licenses/MIT)

Made with ❤️ by [Taiki-Arisue](https://github.com/Taiki-Arisue)

</div>