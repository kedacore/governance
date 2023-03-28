# Governance

## Voting

All decisions made by maintainers have to be a [super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote) where every maintainers representing the same company only have one vote. This enables our project to be neutral and not have a single company have more weight over others.

## Project Maintainers

[Project maintainers](MAINTAINERS.md) are responsible for activities around
maintaining and updating the KEDA. Final decisions on the features
reside with the project maintainers.

Maintainers MUST remain active. If they are unresponsive for >3 months, they
will be automatically removed unless a
[super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote) of
the other project maintainers agrees to extend the period to be greater than 3
months.

If a maintainer violates our [code of conduct](CODE_OF_CONDUCT.md), all maintainers will discuss the incident allowing the maintainer to give background and other maintainers will cast a vote. If the vote results in a  [super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote), then the maintainer needs to step down and leave the maintainer board.

New maintainers can be added to the project by a
[super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote)
vote of the existing maintainers. A potential maintainer may be nominated by an
existing maintainer. A vote is conducted in private between the current
maintainers over the course of a one week voting period. At the end of the week,
votes are counted and a pull request is made on the repo adding the new
maintainer to the [MAINTAINERS](MAINTAINERS.md) file.

Individuals interested in becoming maintainers may submit an [issue](https://github.com/kedacore/governance/issues/new)
stating their interest.  Existing maintainers can choose if they would
like to nominate these individuals to be a maintainer following the process
above.

A maintainer may step down by submitting an
[issue](https://github.com/kedacore/governance/issues/new) stating their intent.

Changes to this governance document require a pull request with approval from a
[super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote) of
the current maintainers.

## Managing Projects

New projects can be added to the organization after a successful
[super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote)
vote of the existing maintainers.

Contributors who want to donate an add-on scaler, sample or donate a repo must
create an issue explaining what the benefit would be for KEDA after which the
maintainers will vote and require a [super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote)
of the current maintainers.

When KEDA wants to archive an existing project, maintainers have to take vote where  a [super-majority](https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote) of the current maintainers agrees to archive the project with a clear indication of why it is being archived. We must not delete projects to avoid customer confusion.

## Scaler Governance

One of the main benefits of KEDA is its [rich catalog of scalers](https://keda.sh/docs/latest/scalers/) which are provided and maintained. Given the wide-range of scalers, KEDA has provided a [dedicated scaler governance](SCALERS.md) to govern them.
