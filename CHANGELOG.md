# Change Log

All notable changes to the "go-katana" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [Unreleased]

- Initial release

## [1.1.0] - 2023-07-15

### Added

- New snippet for create reciver functions `rfunc`
- New snippet for create pointer reciver functions `prfunc`
- New snippet for create constructor `constructor`
- New snippet for create pointer constructor `pconstructor` 
- New snippet for create a Entity with pointer constructor and reciver functions `pentity`
- New snippet for create a Implementation with pointer constructor and reciver functions `pimpl`

### Fixed

### Changed

- The snippet `entity` now generate a Entity without using pointer reciver functions the past `entity` command now renamed to `pentity`
- The snippet `impl` now generate a Implementation without using pointer reciver functions the past `entity` command now renamed to `pimpl`

### Removed