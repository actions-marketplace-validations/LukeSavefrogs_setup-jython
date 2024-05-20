# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v5.1.0] - 2024-05-20

### Added

- Add installer and jython binaries caching
- Add `cache-hit` output value, which is set to `true` if the Jython data/binaries are retrieved from cache.

## [v5] - 2024-05-16

### Added

- Now it is possible to use Jython 2.0 and 2.1 on `ubuntu` and `macos` runners!
- Added support for Powershell on all runners (previously only on `windows` runners)
- Added support for Windows Command Prompt (`cmd`) on windows runners. Notice that because of how the `cmd` handles single quotes it only works if no single quotes are used to enclose parameters: `jython.bat -c "print 'Hello world'"` will work, while `jython.bat -c 'print "Hello world"'` will not.

**Tests**:
- Add tests for Bourne shell (`sh`), Windows Command Prompt (`cmd`) on Windows runners and Powershell (`pwsh` or `powershell`)

### Changed

- Renamed `jython.bat` to `jython.ps1`. To use Jython on the powershell now you have to specifically call `jython.ps1`

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
