# Required Project Files / Configuration

In order to provide community members with everything necessary to succeed in a project we require a minimum set of files and configuration for each project repository. This provide potential users and contributors with information they will need to interact with the project and increases the likelihood of successful project contributions.

## Configuration

### Repository Description

A project should include a useful description that acts as elevator pitch for potential users that may find the project in search engines.

### Repository Topics

GitHub uses repository topics to aid their search engine. Appropriate topics (keywords) for the project should be added to help users find a repository.

### Repository Labels

A project should include [the standard set of labels](github-labels.md) for issues and PRs.

### Disable Unused Features

New GitHub repositories ship with the Projects and Wiki features enabled by default. If these are not being used by a project they should be disabled.

### PR Status Check: Developer Certificate of Origin

All Chef Software Inc. OSS projects use the [developer certificate of origin](/DCO.md) for contributed changes. Commits in a pull request must be signed off by the author(s) to be eligible for merging. You COULD spend the time manually confirming that the developers have signed off on their commits, but it's probably a good idea to automate this with Expeditor or another tool of your choosing.

## Files

See the [oss_project_boilerplate repo](https://github.com/chef/oss_project_boilerplate) for samples of many of these files you can use in your project.

### README.md

A project readme is the first thing a new user or contributor sees when interacting with a Chef Software project. We want to make sure this file is detailed and up to date. It should cover the following things:

  - What the project is itended to be used for.
  - Any system or runtime requirements.
  - Example uses.
  - Known issues or incompatibilies.
  - The Chef team responsible for the project
  - The project license
  - When a product requires a license to run the binary, link to document explaining Chef's licensing terms (license on code is different than license on binary) [This document is still to be written]

### LICENSE

The LICENSE file is an important legal requirement for open source code, and it is also parsed by Github for use in various places. Adding a license file allows users to search for projects with a specific license and also adds licensing badges to GitHub repository pages. Unless there is a specific reason all Chef projects should be [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0.html) licensed.

### CONTRIBUTING.md

GitHub prompts new contributors to read a project's CONTRIBUTING.md file if present. Each project should include a file that details the team specific contribution process and links to the [Contributor Guide](../contributors/README.md) guide in this repository.

### CODE_OF_CONDUCT.md

GitHub displays the code of conduct file when a user opens a new PR or Issue. We want to make sure everyone reads and understands our code of conduct so this needs to be included in every project repository.

### TEAMS.md

The TEAMS file in a repo is commonly seen in other projects as MAINTAINERS.md. Most TEAMS definitions are managed in a [central teams directory](https://github.com/chef/chef-oss-practices/teams). Teams are encouraged to include a `TEAMS.md` in the root of their project repos with links back to the centrally located teams directory.

### .github/CODEOWNERS

The GitHub codeowners file is used to auto assign reviewers to a project. Properly routing new pull requests to the appropriate humans decreases the time it takes to get code reviewed and merged. It also reduces the number of lost pull requests, which helps us engage new contributors and retain them for the future. CODEOWNERS can be setup to assign ownership of certain directories or files to particular teams or individuals. For example, changes to files under `readme/docs` can automatically assign the docs team for review.

### .github/ISSUE_TEMPLATE.md

Issue templates ensure that issues are filed with all the necessary information to make them actionable. GitHub allows including multiple issues, which can be used to provide different templates depending on the issue type (bug, proposal, etc.)

### .github/PULL_REQUEST_TEMPLATE.md

Pull Request templates ensure that the users have followed all the necessary steps before sumitting a PR. They also give us one last chance to point users to our contributing guides so we can ensure first time contributors have a good experience.

## Other Recommendations

### Pull Request Reminders

We find pull request reminders to be a practical mechanism for reminding project members they have open PRs in need of review. Teams should feel free to choose whichever tool for this that they like, but there are two that we recommend.

* GitHub webhooks with Slack - this will update a Slack channel when a new pull request is open (and is highly configurable)

* [Pull Reminders](https://pullreminders.com/) - this will routinely ping reviewers assigned to a pull request until that pull request is either merged or closed. Chef does have a current subscription to this tool