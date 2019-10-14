# Changelog

## [4.0.0](https://github.com/ExtendRealityLtd/VRTK/compare/v3.9.9...v4.0.0) (2019-10-14)

#### :warning: BREAKING CHANGES :warning:

* VRTK is now a UPM package and does no longer directly include Zinnia, instead referencing it as a package dependency. Consumers of VRTK will have to follow the added steps in the README to include VRTK in their projects. ([477b2a7](https://github.com/ExtendRealityLtd/VRTK/commit/477b2a722f0f9ae6f0953fdd3d570d24928184ee))

#### Bug Fixes

* **ci:** back to npmjs.com ([cb21359](https://github.com/ExtendRealityLtd/VRTK/commit/cb21359e839bf6e0ffc75ececbce54905eacf197))
  > GitHub's npm feeds only allow publishing scoped packages, but UPM doesn't support those.

#### Build System

* use Zinnia as dependency package ([477b2a7](https://github.com/ExtendRealityLtd/VRTK/commit/477b2a722f0f9ae6f0953fdd3d570d24928184ee))
  > The content of the dependency Zinnia was copied directly into this project via a git submodule. Keeping dependencies in the project only is necessary in environments that don't offer the idea of a package and a package manager. With Unity nowadays coming with the Unity Package Manager (UPM) VRTK can now become a package, referencing its needed dependency Zinnia as a package dependency.

#### Continuous Integration

* implement continuous delivery ([8872e5a](https://github.com/ExtendRealityLtd/VRTK/commit/8872e5a2dfd51d0a0bde937d28551984e29640a3))
  > Since VRTK is now a UPM package it should automatically be released as one. This change adds automatic creation of UPM packages for VRTK, including automatic SemVer-styled versioning based on the commit messages. A release is both uploaded to the ExtendReality npm GitHub registry as well as an GitHub release (archived .zip). The `package.json` file has been updated to publish beta releases out of the `master` branch, instead of using the CD template's defaults.
