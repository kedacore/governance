# Scaler Governance

This document describes how KEDA handles governance of built-in scalers and how it relates to external scalers maintained by the community.

## Scalers in KEDA

Each event source has unique characteristics on how KEDA needs to connect to it and the types of metrics available to drive scaling. KEDA is made up of many *scalers*, or simple extensions to the core KEDA operator that allows it to connect to an event source.

> 📝 You can find a full list of supported scalers in [our documentation](https://keda.sh/docs/latest/scalers/).

Scalers are shipped with KEDA in two ways:

- **Built-in Scalers** - Scalers are packaged and shipped as part of the core KEDA runtime
- **External Scalers** - Scalers that are running outside of KEDA but are capable of being used to scale workloads with. Workloads can be scaled by using the "External" or "External Push" scalers which integrate with the external scalers by using gRPC to drive scale.

### Choosing the right model for a scaler

When introducing a new scaler, it is important to choose the right model for it - Should it be a built-in scaler or an external scaler?

The general rules of thumb for built-in scalers are the following:

- They must live in the [core KEDA repository](http://github.com/kedacore/keda)
- It follows the [KEDA core release cycle](https://github.com/kedacore/keda/blob/main/ROADMAP.md#upcoming-release-cycles)
- It has no additional infrastructure requirements
- It is general-purpose and not specific to a single end-user
- It is written in Go

If all of the above are true, then it is a potential case for a new built-in scaler. We recommend opening a feature request to propose and discuss it before doing the actual implementation though. This is to avoid throwing things away if it does not meet the needs after all.

### Requirements for a built-in scaler

In order to contribute a scaler to KEDA's core, it must meet the following requirements:

- A scaler MUST be written in Go
- A scaler maintainer(s) MUST be assigned (individual(s)/company) and will be tagged for bug reports. If this is not the case, then it will be considerd to be "community-maintained" and all issues will be tagged with "help-wanted".
- A scaler MUST have e2e and unit tests to guarantee its quality
- A scaler CAN be deprecated when:
  - Maintainers believe it is best for the project, after a vote
  - The scaler maintainer(s) are not responsive and support volume is too high
  - The technology is proven to be no longer used/abandoned
- Scaler MUST follow KEDA release cycles
- A scaler MUST be supported, as per [our support policy](SUPPORT.md), by the scaler maintainer(s) and will be automatically assigned to PRs. This will be done by using GitHub's Codeowners.

### Choosing a home for external scalers

Given the nature of external scalers, we recommend that they are maintained by the community and have a home outside of the KEDA organization. The reason for this is that it sets clear expectations for the community in terms of ownership and support.

There have been exceptions where they have been added to the KEDA organization, but that is because they are governed and co-maintained by the community. Regardless of the fact that they are part of the KEDA organization, the KEDA maintainers are not responsible for them but they work closely together with the scaler maintainers who are responsible for the quality of the scaler, timelines, etc.

Every external scaler inside the KEDA organization will have a liason which acts as a contact person between the KEDA maintainers and scaler maintainers. In case of a need, KEDA maintainers can influence requirements for new releases in order to ensure end-users have the best experience using the scalers in a consistent manner that fits the KEDA ecosystem.

## Building an ecosystem around external scalers

While external scalers are not part of KEDA's core, we highly encourage the community and vendors to build them and make sure they are discoverable.

Artifact Hub allows the community to browse and list external scalers as a "kind" of artifact. Maintainers of external scalers are encouraged to list them in the Artifact Hub as per [the documentation](https://artifacthub.io/docs/topics/repositories/#keda-scalers-repositories).

All external scalers in Artifact Hub are automatically listed on [KEDA's website](https://keda.sh/docs/latest/scalers/) to make sure they are discoverable.
