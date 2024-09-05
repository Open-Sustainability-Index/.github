# Open Sustainability Index

_Open, accessible, transparent, actionable sustainability data._

We believe in open data and open source.

## Do you want to help building Open Sustainability Index?

- Read our [Introduction for new contributors](https://github.com/orgs/Open-Sustainability-Index/discussions/12) in the discussions.
  - Read [how to set up your development environment](https://github.com/Open-Sustainability-Index/open-sustainability-index-frontend?tab=readme-ov-file#how-to-set-up)
  - See development todo list here: https://github.com/orgs/Open-Sustainability-Index/projects/1/views/3
  - See https://www.opensustainabilityindex.org/support-us for more information on how to contribute to Open Sustainability Index.
- See https://www.opensustainabilityindex.org/api on how to access the data through our API.

## Development workflow

- Always work in separate branches, and use pull requests.
- Process:
	1. When starting on new task, assign yourself to the [GitHub task card](https://github.com/orgs/Open-Sustainability-Index/projects/1/views/3) and move the card to “In Progress” lane.
	2. Create new branch for new feature: `dev/[description-of-feature]` (PR title: “Description of feature”) or fix: `dev/fix-[description-of-bug]` (PR title: “Description of bug”).
	3. Apply code linting/prettifier – `npm run fix` – before committing code and correct any issues.
	4. Create [pull request (PR)](https://github.com/Open-Sustainability-Index/open-sustainability-index-frontend/pulls) on GitHub.
	5. Tech Lead will approve pull request and merge into `main` branch.
- It’s ok to merge `main` branch into your feature branch to solve conflicts.
- Versioning (in `package.json`) done by Tech Lead: `v1.2.3` = `v[Major].[Minor].[Patch]`. Minor: when a new screen/page is added, Patch for other changes.

## Communication

We use [GitHub Discussions](https://github.com/orgs/Open-Sustainability-Index/discussions) for communications around development and design of Open Sustainability Index.

Send an email to hello@opensustainabilityindex.org if you have other questions.
