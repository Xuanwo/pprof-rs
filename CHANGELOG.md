# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.7.0] - 2022-03-08

### Added
- Add rust-protobuf support by adding protobuf-codec features (#106)

### Changed
- protobuf feature is renamed to prost-codec to align all other tikv projects (#106)

## [0.6.2] - 2021-12-24
### Added
- implement `Clone` for `ProfilerGuardBuilder` [@yangkeao](https://github.com/YangKeao)
- Add thread names and timing information to protobuf reports [@free](https://github.com/free)

## [0.6.1] - 2021-11-01
### Added
- `blocklist` to skip sampling in selected shared library [@yangkeao](https://github.com/YangKeao)

### Fixed
- Fix memory leak in collector of samples [@yangkeao](https://github.com/YangKeao)

## [0.6.0] - 2021-10-21
### Changed
- Bump prost* to v0.9.0 [@PsiACE](https://github.com/PsiACE)

### Security
- Bump nix to v0.23 [@PsiACE](https://github.com/PsiACE)

## [0.5.0] - 2021-10-21
### Changed
- Bump version of prost* [@PsiACE](https://github.com/PsiACE)

## [0.4.4] - 2021-07-13
### Fixed
- Fix the lifetime mark is not used by criterion output [@yangkeao](https://github.com/YangKeao)

## [0.4.3] - 2021-03-18
### Changed
- Change the output paths for `criterion::PProfProfiler` to support benchmark groups [@yangkeao](https://github.com/YangKeao)

### Security
- Bump nix to v0.20 [@yangkeao](https://github.com/YangKeao)

## [0.4.2] - 2021-02-20
### Added
- Implement criterion profiler [@yangkeao](https://github.com/YangKeao)

### Fixed
- Fix compilation error on arm architecture [@yangkeao](https://github.com/YangKeao)

## [0.4.1] - 2021-02-10
### Added
- Allow passing custom flamegraph options [@yangkeao](https://github.com/YangKeao)

## [0.4.0] - 2020-12-30
### Fix
- Fix flamegraph inline functions [@yangkeao](https://github.com/YangKeao)

## [0.3.21] - 2020-12-28
### Changed
- Bump version of prost* [@xhebox](https://github.com/xhebox)

### Security
- Bump rand to v0.8 @dependabot
- Bump nix to v0.19 @dependabot

## [0.3.20] - 2020-12-11
### Changed
- Split `symbolic-demangle` into multiple features [@yangkeao](https://github.com/YangKeao)

## [0.3.19] - 2020-12-11
### Fix
- Ignore SIGPROF signal after stop, rather than reset to the default handler [@yangkeao](https://github.com/YangKeao)

## [0.3.18] - 2020-08-07
### Added
- Add `Report::build_unresolved` [@umanwizard](https://github.com/umanwizard)

### Changed
- Change from `&mut self` to `&self` in `RpoertBuilder::build` [@umanwizard](https://github.com/umanwizard)

## [0.3.16] - 2020-02-25
### Added
- Support cpp demangle [@yangkeao](https://github.com/YangKeao)

## [0.3.15] - 2020-02-05
### Added
- Filter out signal handler functions [@yangkeao](https://github.com/YangKeao)

### Fixed
- Fix protobuf unit [@yangkeao](https://github.com/YangKeao)

## [0.3.14] - 2020-02-05
### Fixed
- Don't get lock inside `backtrace::Backtrace` [@yangkeao](https://github.com/YangKeao)

## [0.3.13] - 2020-01-31
### Added
- Export `prost::Message` [@yangkeao](https://github.com/YangKeao)

### Fixed
- Only use thread name on linux and macos [@yangkeao](https://github.com/YangKeao)
- Disable `#![feature(test)]` outside of tests [@kennytm](https://github.com/kennytm)

## [0.3.12] - 2019-11-27
### Fixed
- Stop timer before profiler stops [@yangkeao](https://github.com/YangKeao)

## [0.3.9] - 2019-11-08
### Added
- Support profobuf output [@lonng](https://github.com/lonng)

## [0.3.5] - 2019-11-04
### Changed
- Change crate name from `rsperftools` to `pprof-rs` [@yangkeao](https://github.com/YangKeao)

## [0.3.4] - 2019-11-04
### Changed
- Use less stack space [@yangkeao](https://github.com/YangKeao)

## [0.3.2] - 2019-11-01
### Fixed
- Seek to the start before reading file in `TempFdArray`[@yangkeao](https://github.com/YangKeao)

## [0.3.1] - 2019-11-01
### Added
- Support customized post processor for frames [@yangkeao](https://github.com/YangKeao)

### Fixed
- Fix deadlock inside the `std::thread::current().name()` [@yangkeao](https://github.com/YangKeao)

## [0.2.3] - 2019-10-31
### Fixed
- Avoid calling `malloc` inside the signal handler [@yangkeao](https://github.com/YangKeao)

## [0.1.4] - 2019-10-25
### Changed
- Implement `Send` for `Symbol` [@yangkeao](https://github.com/YangKeao)

## [0.1.3] - 2019-10-24
### Added
- Add log [@yangkeao](https://github.com/YangKeao)

### Fixed
- Stop signal handler after processing started [@yangkeao](https://github.com/YangKeao)

## [0.1.1] - 2019-10-22
### Added
- Check whether profiler is running when starting the profiler [@yangkeao](https://github.com/YangKeao)

## [0.1.0] - 2019-10-22
### Added
- Support profiling with signal handler [@yangkeao](https://github.com/YangKeao)
- Support generating flamegraph [@yangkeao](https://github.com/YangKeao)
