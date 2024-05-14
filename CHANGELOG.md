# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Now it is possible to use Jython 2.0 and 2.1 on `ubuntu` and `macos` runners

## [v4] - 2024-05-14

### Fixed

- Fix Jython not working on PowerShell for Windows runners by [@ZZy979](https://github.com/ZZy979) in [#11](https://github.com/LukeSavefrogs/setup-jython/pull/11)
- Fix action failing on macos runners (updated Java 8 distribution to Zulu), add missing shebang by [@ZZy979](https://github.com/ZZy979) in [#10](https://github.com/LukeSavefrogs/setup-jython/pull/10)

## [v3] - 2023-06-08

### Breaking changes

- Renamed action output `jython-download-url` to `download-url`

### Added

- Support for Jython 2.0 and 2.1 (_only on `windows-*` runners_, see [#1](https://github.com/LukeSavefrogs/setup-jython/issues/1))
- Exit with error when provided Jython version does not exist

### Fixed

- `download-url` description now do not have a placeholder text but actually holds meaningful info
