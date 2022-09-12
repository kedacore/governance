# Releases

This document describes how KEDA handles versioning, releases new versions and communicates about them.

KEDA uses semantic versioning so that their users can reliably upgrade according to their needs.

## Release Cycle

KEDA is using a release schedule of 2 to 3 months and uses [GitHub milestones](https://github.com/kedacore/keda/milestones) to provide an indiciation of when the next release is planned. It can, however, happen that releases get delayed which will be reflected on the milestone.

## Release Process

You can learn about our release process [here](https://github.com/kedacore/keda/blob/main/RELEASE-PROCESS.md).

## Keeping Track Of Changes

We provide a changelog that includes every change per version must be available as part of the repo, for example, here is the changelog for [KEDA Core](https://github.com/kedacore/keda/blob/main/CHANGELOG.md).

Next to that, every closed issue and PR should be added to a GitHub Milestone that provides an overview of everything that will be included and provide an indication of what the current intended release date is. However, the release date is subject to change and only provides an indication.

Lastly, every new release will come with a GitHub Release which provides the exact changelog for that release.

## Get Notified For New Releases

If you want to be notified of new releases, we recommend [watching](https://docs.github.com/en/github/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#configuring-your-watch-settings-for-an-individual-repository) our [KEDA Core repository](https://github.com/kedacore/keda) on GitHub and ensure you are subscribing for releases.

Next to that, you can join the conversation for every new release on [GitHub Discussions](https://github.com/kedacore/keda/discussions/categories/announcements).

## Removing Features, Breaking Changes & Deprecations

Every new major version, KEDA maintainers are allowed to remove features or make breaking changes as per [semantic versioning](https://semver.org/).

Along with such a release there will always be a migration guide to provide an overview of what has changed, what the impact is and how to migrate. Here is an example of our v1.x to v2.0 migration guide ([example](https://keda.sh/docs/latest/migration/)).

For every one of these, KEDA will always announce a deprecation notice on [GitHub Discussions](https://github.com/kedacore/keda/discussions/categories/deprecations) that provides context on why it is changing, what the impact is, when it will change and what steps that are required to be taken.

In majority of the cases, we will allow you to already migrate in the next minor version where we introduce the deprecation so that you can migrate fast.

## Support

Learn more about our support policy [here](https://github.com/kedacore/governance/blob/main/SUPPORT.md).
