# Deprecations & Breaking Changes in KEDA

This document describes how KEDA handles deprecations and breaking changes and should provide clarity to KEDA end-users on what to expect when upgrading to a new version of KEDA.

If you are interested in the current open deprecations, we recommend checking our [GitHub Discussions](https://github.com/kedacore/keda/discussions/categories/deprecations) or the open breaking changes](https://github.com/kedacore/keda/issues?q=is%3Aopen+label%3Abreaking-change+sort%3Aupdated-desc).

## Our versioning strategy

KEDA follows the [Semantic Versioning](https://semver.org/) strategy and can only introduce breaking changes in new major versions.

However, depending on the nature of the change, we may introduce deprecations in existing minor versions. These changes always must be backwards-compatible.

Depending on the area of the change, we might not need to wait for the next major version of KEDA to introduce a breaking change.

### KEDA runtime

The KEDA runtime, which consists of the operator and metric server, is not allowed to make breaking changes unless the major version is incremented.

There are no exceptions to this rule.

### Custom Resource Definitions (CRDs)

Our custom resource definitions (CRDs) have a separate versioning scheme than the KEDA runtime given they have an `apiVersion`. For this, we follow the [official Kubernetes API versioning policy](https://kubernetes.io/docs/reference/using-api/#api-versioning).

KEDA is allowed to make breaking changes to the CRDs, when a new `apiVersion` is introduced.

However, the KEDA runtime must support all current API versions until the next major version of KEDA.

### Autoscaling triggers and their metadata

Until KEDA introduces a [versioning scheme for autoscaling triggers](https://github.com/kedacore/keda/issues/613), it is not allowed to make breaking changes for triggers.

The only exception to this rule is when a new `apiVersion` is introduced.

### Helm chart

The Helm charts that KEDA provides have a seperate release & version lifecycle. They follow [Semantic Versioning](https://semver.org/) but specifically around the Helm charts and is versioned independently from the KEDA runtime.

### Kubernetes compatibility

As per our [Kubernetes compatibility](https://keda.sh/docs/latest/operate/cluster/#kubernetes-compatibility) policy, we provide support for Kubernetes N-2.

This means that a minor version upgrade of KEDA is backwards-compatible with Kubernetes N-2, but might remove support for an older version.

This kind of change will be announced in the release notes and enforced in our Helm charts.

## What is considered a breaking change?

A breaking change is a change that is not backwards-compatible and requires end-users to take manual action to migrate or lose existing functionality.

## Avoiding breaking changes

When contributors want to introduce a new approach, they are allowed to do so without breaking changes. This means that the new approach will be available in the next minor version of KEDA but the existing functionality still works.

Every occasion of this must provide warning(s) in the KEDA logs to make customers aware of the change so they can decide whether to migrate to the new approach - Either by using the new functionality in the next minor version or by migrating to the new approach when the next major version was released.

Every deprecation must follow our process described below.

## Introducing new deprecations

When introducing a new deprecation, it must comply with the following rules:

- Every deprecation must be announced in the release notes and will be highlighted in the upcoming release
- Every deprecation must have a warning in the KEDA logs to create awareness
- Every deprecation must have a representing issue that is used for tracking breaking changes for our upcoming major version. Because of that, it must be labeled with [`breaking-change`](https://github.com/kedacore/keda/issues?q=is%3Aopen+label%3Abreaking-change+sort%3Aupdated-desc).
- Every deprecation must be announced on [GitHub Discussions](https://github.com/kedacore/keda/discussions/categories/deprecations) ([example](https://github.com/kedacore/keda/discussions/3552))
  - It should explain when the deprecation takes effect, what the impact is, how to migrate and when it will be removed.