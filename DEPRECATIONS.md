# Deprecations & Breaking Changes in KEDA

This document describes how KEDA handles deprecations and breaking changes and should provide clarity to KEDA end-users on what to expect when upgrading to a new version of KEDA.

## TODO

- Changes should be done in a backward-compatible fashion, deprecated and removed later on
- Once things are deprecated, they should be:
  - Announced on GitHub discussions (similar to https://github.com/kedacore/keda/discussions/3552)
  - Have a warning in the KEDA logs
  - Have an entry in the deprecation section of our changelog
  - Have a callout in our GitHub release (similar to https://github.com/kedacore/keda/releases/tag/v2.8.0)
  - Have a representing issue that is tracked to remove it (labeled with `breaking-change`)