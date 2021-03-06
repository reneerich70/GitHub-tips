# GitHub Tips by Chingu

[Credits](AUTHORS.md) ∙ [Contributing guidelines](CONTRIBUTING.md)


## Table of Contents

- [Purpose](#the-purpose-of-this-repo)
- [About Chingu](#the-chingu-github-organization)
- [Collaborating on GitHub](#collaborating-on-github---a-tale-of-two-models)
- [GitHub Organizations](#working-with-organizations)

## The Purpose of this Repo

GitHub.com is an amazing code collaboration platform which has enabled several open source project to flourish. Contributing to projects on GitHub for those new to the platform, however, can be both intimidating and confusing. This repo aims to provide some clarity on the features and workflows of GitHub.

There is no intention to re-invent the wheel however! So a visit to GitHub's own learning resources [described here](#github-flow-tutorial) is a top recommendation.


## The Chingu GitHub Organization

[Chingu](https://tropicalchancer.github.io/projectus/) is a self-organizing coding bootcamp community and innovative collaboration project. It's also now a GitHub organization! The reasons for this organization's existence include the following:

1. Provide Chingu members with a safe place to practice and participate in code collaboration workflows
2. Deliver visibility to all Chingu members on what their peers are working on and have accomplished
3. Curate a refined selection of resources to support Chingu members in achieving their learning and career goals

## Collaborating on GitHub - A Tale of Two Models

There are two predominate models for collaborating on GitHub projects:

 * **[Fork & Pull Model](https://en.wikipedia.org/wiki/Fork_and_pull_model)**: This is the predominate model used by open-source projects on GitHub. The project has a core group of project maintainers but many more potential contributors. The high-level workflow involves:

    1. Contributor [forks](https://help.github.com/articles/fork-a-repo/) the main project repo to their user account
    1. Contributor creates a [branch](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) and completes their work locally (more on this later)
    1. Contributor [pushes](https://help.github.com/articles/pushing-to-a-remote/) to their user account and submits a [pull request](https://help.github.com/articles/about-pull-requests/) (PR)
    1. Project maintainer is notified of PR and one or more of several things can happen next - discussion on the PR, continuous integration (CI) tests, acceptance of the PR (with or without edits), rejection of the PR

 * **Shared Repository Model**: In this model, everyone works on the same repo and there is no forking. The advantage is decreased complexity with the drawback of less control. This model is ideal for projects where the expected contributors are already known - for example - the Chingu build.to.learn projects! The high-level workflow involves:

    1. Contributor creates a branch and completes their work locally (details to come)
    1. Contributor pushed branch to shared repo
    1. Contributor creates a pull request (PR) into master from their branch, optionally [assigning a reviewer](https://help.github.com/articles/assigning-issues-and-pull-requests-to-other-github-users/)
    1. Reviewer is notified of PR and one or more of several things can happen next - discussion on the PR, continuous integration (CI) tests, acceptance of the PR (with or without edits), rejection of the PR

For both models, [different rules](https://help.github.com/articles/enabling-required-status-checks/) can be created as to what is required before acceptance of a PR and corresponding merge of changes into the master branch. In any case, directly pushing to master from local is either not allowed or just not good practice as it prevents the opportunity for conservation and code review on the desired changes.

Both of these workflows follow what is called "GitHub flow" illustrated here in this [GitHub guide](https://guides.github.com/introduction/flow/).

### GitHub Flow Tutorial

Want an easy introduction to GitHub with an actual repository? GitHub has created a great tutorial provided through their [On Demand Training site](https://services.github.com/on-demand/). Just complete the **GitHub 101: Introduction to GitHub** course and you will have completed a contribution to a real repository using GitHub flow. Can you identify if it uses the "Fork & Pull" or "Shared Repository" model.

GitHub also hosts many other [learning resources](https://services.github.com/resources/learning-path/) as well as a [GitHub cheat sheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf).

## Working with Organizations

Note: Much of this is distilled from the [information provided here](https://help.github.com/categories/setting-up-and-managing-organizations-and-teams/)

### Organization and Roles

We have started with an organization for all the Chingu coders. All members who requested access were added with the **Member** role. With the **Member** role, you can:

1. Create repos
1. Create teams and be made a team maintainer
1. See all members and teams
1. Create or delete project boards and edit descriptions

There is also the **Owner** role who can invite and delete members, add billing information and delete the organization. This role will be provided on request to cohort leads and others with the need and to apply these features.

### Teams and Organization Repos

Although all members can create organization repo, they must specifically manage permissions on that [repo for each member](https://help.github.com/articles/repository-permission-levels-for-an-organization/#changing-repository-settings]) they want to collaborate with. An option to better organize permissions on multiple repos is the use of **Teams**.

*Any* organization member can create a team.

**To create a Team**:

1. Go to the ``Teams`` tab and click the ``New team``.
1. In the ``Create new team`` window you can at this point select a ``Parent team``. If left unselected, the parent will be the organization itself. Even if the team has a parent, each team must have a unique name within the *organization* (so you can't have, for example, both "llamas/team1" and "dolphins/team1")
1. At this point you can add one or more members, a repository or even a sub-team.

**To add a member**:

1. Click on **Add a member** button then search by username, full name or email.
1. Click on the user to add them, you will be prompted for your password before continuing.
1. If they are in the organization they will automatically added. If they are not, then an invite will be sent to them which they must accept. For more [see the docs](https://help.github.com/articles/adding-organization-members-to-a-team/).
1. After adding, team members can be promoted to the **Maintainer** role. Maintainers have the [following permissions](https://help.github.com/articles/repository-permission-levels-for-an-organization/#team-maintainers).

**To create an organization/team repo**:

1. From the organization's main page click ``New repository`` or if already on the ``Repositories`` tab click ``New``
1. Enter a name, for example "llamas-b2l-team2-splash", and click ``Create Repository``. You can also optionally initialize the repo with a [README.md](https://gist.github.com/zenorocha/4526327) at this point.
1. To add the repo to a team, within the repo page navigate to **Settings** then **Collaborators & team**. Select the team from the ``Add a team`` drop-down (or create it now). Note: you must be a member of that team or organization owner to do so.
1. Select the team permission level - those with ``Write`` permission can complete most activity required for collaborative coding. More about repository permission levels can be [read here](https://help.github.com/articles/repository-permission-levels-for-an-organization/).

It is important to note that the repo still "belongs" to the organization and thus the repo name must be unique. For example, you cannot have both "llamas-b2l-team2/*splash-page*" and "dolphins-b2l-team4/*splash-page*". The primary value of teams is thus to organize users who should have like permissions, instead of organizing repos.

TODO: Add diagram about relationships between different components.

TODO: Add details about projects