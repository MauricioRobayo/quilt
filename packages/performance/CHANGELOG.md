# Changelog

## 3.1.0

### Minor Changes

- [#2413](https://github.com/Shopify/quilt/pull/2413) [`21435a256`](https://github.com/Shopify/quilt/commit/21435a2562822ef76d3ede49c8b1eaefc1fe475d) Thanks [@rorans](https://github.com/rorans)! - Introduce a RedirectDuration metric to get more specific server latency timings. This information will be sent via TTFB metadata. No changes need to be made on the consumer.

## 3.0.2

### Patch Changes

- [#2408](https://github.com/Shopify/quilt/pull/2408) [`2094cb39a`](https://github.com/Shopify/quilt/commit/2094cb39a674d38a19394b79bf59c11a65ff9e15) Thanks [@BPScott](https://github.com/BPScott)! - Internal typing adjustments as a result of updating Typescript

## 3.0.1

### Patch Changes

- [#2389](https://github.com/Shopify/quilt/pull/2389) [`03c1abc8c`](https://github.com/Shopify/quilt/commit/03c1abc8c293d4c79f34796f9eefc777812df532) Thanks [@BPScott](https://github.com/BPScott)! - Add types field to package.json export maps to support typescript consumers that use `moduleResolution: "node16"`

## 3.0.0 - 2022-05-19

### Breaking Change

- Drop support for node 12 and Safari 10, 11 and 12. Remove wildcard export in exports field. [[#2277](https://github.com/Shopify/quilt/pull/2277)]

## 2.0.14 - 2022-03-09

### Changed

- Correct wildcard export to `./*` [[#2209](https://github.com/Shopify/quilt/pull/2209)]

## 2.0.13 - 2022-02-25

### Changed

- Use `./*` instead of `./` in package.json exports to fix deprecation warning. [[#2184](https://github.com/Shopify/quilt/pull/2184)]
- Remove devDependency on `@shopify/useful-types` by using built-in types. [[#2163](https://github.com/Shopify/quilt/pull/2163)]

## 2.0.12 - 2022-02-01

### Changed

- Rerelease after failed publish. No code changes.

## 2.0.11 - 2022-02-01

### Changed

- Reorder exports map to prioritize the `esnext` condition. [[#2148](https://github.com/Shopify/quilt/pull/2148)]
- Update Loom build config. [[#2150](https://github.com/Shopify/quilt/pull/2150)]

## 2.0.10 - 2021-11-30

- No updates. Transitive dependency bump.

## 2.0.9 - 2021-11-25

### Fixed

- Fixed the "Deprecated API for given entry type." warnings [[#2093](https://github.com/Shopify/quilt/pull/2093)]
- Fixed the "The PerformanceObserver does not support buffered flag with the entryTypes argument" warnings [[#2089](https://github.com/Shopify/quilt/pull/2089)]

## 2.0.8 - 2021-11-23

- No updates. Transitive dependency bump.

## 2.0.7 - 2021-11-22

### Changed

- Fixed babel helpers file being generated with incorrect filename in esm build. [[#2082](https://github.com/Shopify/quilt/pull/2082)]

## 2.0.6 - 2021-09-24

### Changed

- Migrate from `sewing-kit-next` to `loom` for building - package build output remains identical. [[#2039](https://github.com/Shopify/quilt/pull/2039)]

## 2.0.5 - 2021-08-26

### Changed

- Enable type checking in tests and fix type errors. [[#2011](https://github.com/Shopify/quilt/pull/2011)]

## 2.0.4 - 2021-08-24

### Changed

- Updated build tooling, types are now compiled with TypeScript 4.3. [[#1997](https://github.com/Shopify/quilt/pull/1997)]
- Added file exclusion for tests to package.json and enable type checking for tests. [[#2005](https://github.com/Shopify/quilt/pull/2005)]
- Rename test/ to tests/ [[#2005](https://github.com/Shopify/quilt/pull/2005)]

## 2.0.3 - 2021-08-04

### Changed

- Ensure `tsconfig.tsbuildinfo` file is not uploaded to the npm registry. [[#1982](https://github.com/Shopify/quilt/pull/1982)]. [[#1982](https://github.com/Shopify/quilt/pull/1982)]

## 2.0.2 - 2021-08-03

### Changed

- Update to latest sewing-kit-next for build. Update `types`/`typesVersions` fields to point directly into the build folder [[#1980](https://github.com/Shopify/quilt/pull/1980)]

## 2.0.0 - 2021-05-21

### Breaking Change

- Update minimum supported node version to 12.14.0. Add engines field to help enforce usage of this version. [#1906](https://github.com/Shopify/quilt/pull/1906)

## 1.3.4 - 2021-04-13

### Changed

- Removed dependency on tslib, as we no-longer compile with `tsc`. [#1829](https://github.com/Shopify/quilt/pull/1829)

## 1.3.2 - 2021-03-03

### Fixed

- Updated multi-build outputs to include mandatory extensions to fix "Module not found" issues reported by ESM supported bundlers [#1759](https://github.com/Shopify/quilt/pull/1759)

## 1.3.0 - 2020-12-18

### Added

- Add new build outputs (CommonJS, ESM, esnext, Node) for greater tree-shakability [#1698](https://github.com/Shopify/quilt/pull/1698)

## 1.2.10 - 2020-10-20

- Added `tslib@^1.14.1` in the list of dependencies. [#1657](https://github.com/Shopify/quilt/pull/1657)

## 1.2.2 - 2019-10-16

### Fixed

- `Performance` object constructor will now check if `PerformanceTiming` is supported. [[#1119](https://github.com/Shopify/quilt/pull/1119)]

## 1.2.1 - 2019-10-11

### Fixed

- `cacheEffectiveness` now assumes duration=0 is a cache hit [[#1107](https://github.com/Shopify/quilt/pull/1107)]

## 1.2.0 - 2019-10-03

### Changed

- Updated the README to include instructions on cleaning up listeners from `performance.on` [[#1081](https://github.com/Shopify/quilt/pull/1081)

### Added

- Added a new API `mark` to the `Performance` class. This encapsulates both checking for `supportsMarks` and calling `window.performance.mark` into one call. [[#1083]](https://github.com/Shopify/quilt/pull/1083/files)

## 1.1.2 - 2019-03-27

### Fixed

- Fixed an issue where changing only the hash/ query parameters would cause navigations to be recorded [[#610](https://github.com/Shopify/quilt/pull/610)]

## 1.1.1 - 2019-03-04

### Fixed

- Fixed an issue where events starting before the navigation would include the pre-navigation time in `Navigation#totalDurationByEventType` [[#549](https://github.com/Shopify/quilt/pull/549)]

## 1.1.0 - 2019-03-02

### Added

- New `fid` lifecycle event to track [first input delay](https://github.com/GoogleChromeLabs/first-input-delay) (to use this, consumers must inject [polyfill code](https://raw.githubusercontent.com/GoogleChromeLabs/first-input-delay/master/dist/first-input-delay.min.js) into their document head) [[#542](https://github.com/Shopify/quilt/pull/542)]

## 1.0.4 - 2019-02-21

### Fixed

- Fixed an issue where `Navigation#timeToUsable` did not account for when the navigation actually started, leading the values in the trillions [[#520](https://github.com/Shopify/quilt/pull/520)]

## 1.0.3 - 2019-01-11

### Fixed

- Fixed an issue where browsers supporting some custom timing types (but not `PerformanceObserver`) would throw while trying to create an instance of `PerformanceObserver`

## 1.0.2 - 2019-01-11

### Fixed

- The types for `Navigation#resourceEvents` no longer fails in consuming projects.

## 1.0.1 - 2019-01-11

### Fixed

- No longer fails if the browser does not have `window.performance`.

## 1.0.0 - 2019-01-30

First version.
