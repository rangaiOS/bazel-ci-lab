# Bazel CI Lab

A sample C++ project demonstrating Bazel 9.1 build automation, unit testing, and CI/CD integration using GitHub Actions.

## Overview

This repository showcases:

* Bazel 9.1 with Bzlmod
* C++17 project structure
* Unit testing with GoogleTest
* GitHub Actions CI pipeline
* Build caching strategies
* Automated build and test validation

## Tech Stack

| Component      | Version |
| -------------- | ------- |
| Bazel          | 9.1.0   |
| C++            | C++17   |
| GoogleTest     | 1.17.0  |
| GitHub Actions | Latest  |
| Ubuntu Runner  | 22.04   |

## Project Structure

```text
bazel-ci-lab/
├── .github/
│   └── workflows/
│       └── ci.yml
├── src/
│   └── math/
│       ├── BUILD.bazel
│       ├── calculator.h
│       └── calculator_test.cc
├── BUILD.bazel
├── MODULE.bazel
├── MODULE.bazel.lock
├── .bazelrc
└── .gitignore
```

## Build

Build all targets:

```bash
bazel build //...
```

Build a specific target:

```bash
bazel build //src/math:calculator
```

## Run Tests

Execute all tests:

```bash
bazel test //...
```

Run a specific test:

```bash
bazel test //src/math:calculator_test
```

## CI Pipeline

The GitHub Actions workflow automatically runs on:

* Pull Requests
* Pushes to main

Pipeline stages:

1. Checkout source code
2. Setup Bazelisk
3. Restore cache
4. Build all targets
5. Run unit tests
6. Upload test artifacts

## Why Bazel?

Bazel provides:

* Hermetic builds
* Incremental compilation
* Parallel execution
* Reproducible builds
* Efficient CI/CD pipelines

## Learning Objectives

This project demonstrates:

* Bazel workspace configuration
* BUILD.bazel authoring
* Bzlmod dependency management
* GoogleTest integration
* GitHub Actions automation
* Build cache optimization

## References

* Bazel Official Documentation
* Bazel Central Registry (BCR)
* GoogleTest Documentation

## Author

Ranganath Chenna
GitHub: https://github.com/rangaiOS
