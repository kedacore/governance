# Governance

## Voting

All decisions made by maintainers have to be a [super-majority][super-majority] where every maintainers representing the same company only have one vote. This enables our project to be neutral and not have a single company have more weight over others.

## Project Maintainers

### Responsibilities & Expectations

[Project maintainers][maintainers] are responsible for activities around maintaining, evolving and keeping KEDA secure. Given the responsibility they have, final decisions on the features/changes/proposals reside with the project maintainers.

Existing and potential maintainers are expected to do the following:

- **Actively contribute to the project** which can be in various ways. Contributions should be consistent over at least two months.
  - Examples of valuable contributions are writing code/tests, writing documentation, governance, triaging issues, review code, automating processes and workflows, etc.
- **Join our [bi-weekly standups][standup] regularly**
- **Respect our [Code of Conduct][code-of-conduct]**
- Although not binding, but introducing more end-user representation is beneficial

Maintainers MUST remain active. If they are unresponsive for >3 months, they can be automatically removed unless a
[super-majority][super-majority] of the other project maintainers agrees to extend the period to be greater than 3 months.

If a maintainer violates our [Code of Conduct][code-of-conduct], all maintainers will discuss the incident allowing the maintainer to give background and other maintainers will cast a vote. If the vote results in a [super-majority][super-majority], then the maintainer needs to step down and leave the maintainer board.

### Becoming A Maintainer

New maintainers can be added to the project by a [super-majority][super-majority]
vote of the existing maintainers after a potential maintainer was nominated by an existing maintainer. A vote is conducted in private between the current maintainers over the course of a two weeks voting period, unless one or more maintainers are on time off. At the end of the week, votes are counted and a pull request is made on the repo adding the new maintainer to the [MAINTAINERS](MAINTAINERS.md) file once the voting has a [super-majority][super-majority].

Individuals interested in becoming maintainers may submit an [issue][create-governance-issue] stating their interest.  Existing maintainers can choose if they would like to nominate these individuals to be a maintainer following the process above.

### Stepping Down As A Maintainer

A maintainer may step down by submitting an [issue][create-governance-issue] stating their intent.

## Managing Projects

New projects can be added to the organization after a successful [super-majority][super-majority] vote of the existing maintainers.

Contributors who want to donate an add-on scaler, sample or donate a repo must create an issue explaining what the benefit would be for KEDA after which the maintainers will vote and require a [super-majority][super-majority] of the current maintainers.

When KEDA wants to archive an existing project, maintainers have to take vote where  a [super-majority][super-majority] of the current maintainers agrees to archive the project with a clear indication of why it is being archived. We must not delete projects to avoid customer confusion.

## Scaler Governance

One of the main benefits of KEDA is its [rich catalog of scalers][scaler-catalog] which are provided and maintained. Given the wide-range of scalers, KEDA has provided a [dedicated scaler governance][scalers] to govern them.

## Proposing Governance Changes

Changes to this governance document require a pull request with approval from a
[super-majority][super-majority] of
the current maintainers.

[code-of-conduct]: CODE_OF_CONDUCT.md
[create-governance-issue]: https://github.com/kedacore/governance/issues/new
[maintainers]: MAINTAINERS.md
[scaler-catalog]: https://keda.sh/docs/latest/scalers/
[scalers]: SCALERS.md
[standup]: https://keda.sh/community/
[super-majority]: https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote