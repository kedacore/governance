# Governance

## Community Roles

### Repo Reviewer

A Repo Reviewer is a community member who has been consistently contributing to a specific KEDA repository over a period of 3–6 months. Contributions can include code, documentation, issue triaging, and regular engagement in PR reviews or discussions.

**Responsibilities:**

- Provide meaningful reviews and feedback on pull requests
- Triage and manage issues
- Contribute with code or documentation
- Approve or reject pull requests (valid review)
- In the case of the `keda` core repository, run end-to-end (e2e) tests

**Requirements:**

- Demonstrated regular contributions to a specific repository over 3–6 months

### Repo Maintainer

A Repo Maintainer is a trusted contributor who has served as a Repo Reviewer and has demonstrated long-term commitment and leadership in a given repository for an additional 3–6 months.

**Responsibilities:**

- Approve and merge pull requests
- Participate in repository-scoped decision making
- Lead releases and maintain release quality
- Onboard and mentor new contributors
- Maintain overall repository health and roadmap
- **Join our [bi-weekly standups][standup] regularly**
- **Respect our [Code of Conduct][code-of-conduct]**

**Requirements:**

- History of consistent contributions as a Repo Reviewer (3–6 months)
- Demonstrated understanding of the repository’s scope and architecture

### Organization Maintainers

Organization Maintainers are responsible for the overall direction, health, and governance of the KEDA project and organization.

**Requirements:**

- Must be an active Repo Maintainer in at least two repositories
- Must be contributing to at least three repositories in total

**Responsibilities:**

- Set the strategic direction and priorities for the project
- Make decisions that span across multiple repositories
- Maintain the inclusiveness, openness, and health of the community
- Approve and coordinate project-wide initiatives
- Resolve escalated issues and disagreements
- Nominate and vote on new maintainers
- Act as maintainer for all repositories

### Considerations

Community members MUST remain active. If they are unresponsive for >3 months, they can be automatically removed unless a
[super-majority][super-majority] of the project maintainers agrees to extend the period to be greater than 3 months.

If a member violates our [Code of Conduct][code-of-conduct], all maintainers will discuss the incident allowing the member to give background and maintainers will cast a vote. If the vote results in a [super-majority][super-majority], then the member needs to step down and leave the maintainer board (if they'd be maitainer).

## Voting

All decisions made by maintainers have to be a [super-majority][super-majority] where every maintainers representing the same company only have one vote. This enables our project to be neutral and not have a single company have more weight over others. 

**Note:** If there isn't any consensus between all the maintainers involved in the discussion (project maintainers in the scope of the decision and organization maintainers), another vote will be casted only including organization maintainers.

#### Approving & Merging PRs

Maintainers will approve PRs only when:

- It meets the [scaler requirements](https://github.com/kedacore/governance/blob/main/SCALERS.md)
- It meets the [deprecation/breaking change requirements](https://github.com/kedacore/governance/blob/main/DEPRECATIONS.md)
- It is in line with the goal of the project
- It does not violate the [code of conduct](https://github.com/kedacore/governance/blob/main/CODE_OF_CONDUCT.md).

Apart from the conditions above, all the required checks in the PR have to pass. Maintainers still have the right to merge a PR with one or more failing checks if they, after reviewing the check, consider that it's an unrelated failure (like a transient failure on an e2e test).

In case of dispute, other maintainers are requested to review and agree what the best outcome is of a PR.

Repositories with 5 or more members require at least 2 approvals to merge changes which are not explicitly small (dependencies bumps, a few lines fixes, etc)

### Becoming a member

New members can be added to the project by a [super-majority][super-majority]
vote of the existing maintainers after a potential member was nominated by an existing maintainer. A vote is conducted in private between the current maintainers over the course of a two weeks voting period, unless one or more maintainers are on time off. At the end of the week, votes are counted and a pull request is made on the repo adding the new member to the [Members](MEMBERS.md) file once the voting has a [super-majority][super-majority].

Individuals interested in becoming a member may submit an [issue][create-governance-issue] stating their interest.  Existing maintainers can choose if they would like to nominate these individuals to be a maintainer following the process above.

### Stepping Down As A Maintainer

A member may step down by submitting an [issue][create-governance-issue] stating their intent.

## Managing Projects

New projects can be added to the organization after a successful [super-majority][super-majority] vote of the existing maintainers.

Contributors who want to donate an add-on scaler, sample or donate a repo must create an issue explaining what the benefit would be for KEDA after which the maintainers will vote and require a [super-majority][super-majority] of the current maintainers.

When KEDA wants to archive an existing project, maintainers have to take vote where  a [super-majority][super-majority] of the current maintainers agrees to archive the project with a clear indication of why it is being archived. We must not delete projects to avoid customer confusion.

## Scaler Governance

One of the main benefits of KEDA is its [rich catalog of scalers][scaler-catalog] which are provided and maintained. Given the wide-range of scalers, KEDA has provided a [dedicated scaler governance][scalers] to govern them.

## Proposing Governance Changes

Changes to this governance document require a pull request with approval from a
[super-majority][super-majority] of
the current organization maintainers.

[code-of-conduct]: CODE_OF_CONDUCT.md
[create-governance-issue]: https://github.com/kedacore/governance/issues/new
[maintainers]: MAINTAINERS.md
[scaler-catalog]: https://keda.sh/docs/latest/scalers/
[scalers]: SCALERS.md
[standup]: https://keda.sh/community/
[super-majority]: https://en.wikipedia.org/wiki/Supermajority#Two-thirds_vote
