# Contributing to ILM

We encourage everyone to make contributions to the ILM platform. You can be a part of the community and improving the security of the internet. Your contribution is important to enhance the platform and make it more affordable and available for all of us using digital certificate.

We use [GitHub](https://github.com/) to manage the ILM project and all source codes, including tracking issues.

## Source code management

[GitHub](https://github.com/) is used as version control system.
We use [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow) as our branching strategy. Feature branches are created from `main`, and merged back via pull requests after review.

## Issues

All issues are managed in the respective [GitHub](https://github.com/) repositories.
We use pre-defined issue templates and proper labelling to benefit from the automation process of assigning issues to the right team and to generate the proper reports. Therefore each issue should be labelled with the appropriate labels.

Opening a new issue in any repository of the organization offers the shared templates — **Bug**, **Feature**, **Task**, **Epic**, **Release**, **Documentation** and **QA** — which are maintained centrally in this repository under `.github/ISSUE_TEMPLATE/`. Each is a form: fill in the fields it asks for and the labels and routing are applied for you.

### How to report a vulnerability

**Do not report an undisclosed vulnerability in a public issue.** Report it privately: open the **Security** tab of the affected repository and choose **Report a vulnerability**, or email [ilm@omnitrust.com](mailto:ilm@omnitrust.com). The [security policy](SECURITY.md) describes what to include, when to expect a reply, and how disclosure is coordinated.

The **Vulnerability** issue template is only for vulnerabilities that are already public, such as a CVE raised by dependency or container image scanning.

Our development process includes automated vulnerability management: dependency checks, static analysis of the code, secret detection, and vulnerability scanning of published artifacts. We monitor the common CVE databases for issues affecting the platform and its dependencies.

### How to report a bug

If you find a bug in the platform, you can report it by creating a new issue. Please make sure that the bug is not already reported by checking the list of current issues. If you find the bug is already reported, you can add a comment to the existing issue.

Here are some notes on how to report the bug, so we can fix it as soon as possible:
- Describe the bug in detail, including the steps to reproduce it.
- Include what you expected to happen, as well as what actually happened.
- If it's a bug related to frontend, please include information on what browser version and operating system you are running.
- If you thing it helps, feel free to attach screenshots, or other files illustrating the issue.
- Include context information, such as the version of the components you are using.

### How to suggest a feature or improvement

Your are welcome to enhance the platform by adding new features. You can crate a pull request with the new feature. Do not forget to look into the list of current issues to find out of the feature is already implemented or someone is working on it. If you would like to discuss the feature, use the issue tracker to start a discussion.

We are working on many repositories written in different programming languages. You should use corresponding coding conventions and best practices for the language you are working on.

Our team is monitoring the issues and pull requests regularly. We will provide feedback and help you to get your feature implemented.

Here are some notes on how to suggest a feature or improvement:
- Describe the feature in detail, including the use case and the benefits.
- Include any relevant information that can help us to understand the feature.
- If you have any ideas on how to implement the feature, please include them.
- Include context information, such as the version of the components you are using.
- If you are planning to implement the feature, please let us know so we can help you with the process.

## Contributing for the first time

If you are contributing to ILM for the first time, you can learn how to create a pull request by following [Open Source Guide](https://opensource.guide/how-to-contribute/). This guide will help you to understand the process of contributing to open source projects.

To help you get your feet wet and get you familiar with our contribution process, we have a list of good first issues that contain bugs that have a relatively limited scope. This is a great place to get started.

If you decide to fix an issue, please be sure to check the comment thread in case somebody is already working on a fix. If nobody is working on it at the moment, please leave a comment stating that you intend to work on it so other people don't accidentally duplicate your effort.

## Sign your commits

Every commit must carry a `Signed-off-by` line certifying that you have the right to submit
the work under the project's license. This is the
[Developer Certificate of Origin](https://developercertificate.org/) (DCO) — a statement about
the origin of the contribution, not a copyright assignment. Git adds the line for you with the
`-s` flag:

```
git commit -s -m "Fix the certificate chain ordering"
```

The line uses your configured name and email, which must match the commit author:

```
Signed-off-by: Your Name <you@example.com>
```

Set them once if you have not already:

```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### If you forget

Amend the most recent commit:

```
git commit --amend -s --no-edit
```

Sign off every commit on your branch at once, then force-push. Rebase onto the branch you
opened the pull request against — `main` in most repositories, `develop` in the appliance and
`ansible-role-*` repositories:

```
git rebase --signoff main
git push --force-with-lease
```

Commits made through the GitHub web interface are signed off automatically, so accepting a
review suggestion or using **Update branch** needs nothing from you.

## Development process in steps

The following steps should generally be followed for all development tasks:

1. Clone or fork the repository and create your branch
2. Add your code to the branch
3. Prepare tests for your code (if needed)
4. Make sure your code is written according to the conventions
5. Ensure your code builds and the tests pass
6. Do not commit files and folders unrelated to the code
7. Sign off your commits (see above) and create a pull request

## Commit guidelines

It is a recommended best practice to keep your changes as logically grouped as possible within individual commits. There is no limit to the number of commits any single PR may have, and many contributors find it easier to review changes that are split across multiple commits. Multiple commits get squashed when they are going to be merged.

We are using the following rules for commits:

- Commit Related Changes
- Commit Often
- Don't Commit Half-Done Work
- Test Your Code Before You Commit
- Write Good Commit Messages
- Use Branches
- Always Link Commits

### Commit format

- Capitalized, short (50 chars or less) summary
- More detailed explanatory text, if necessary. Wrap it to about 72 characters. In some contexts, the first line is treated as the subject of an email and the rest of the text as the body. The blank line separating the summary from the body is critical (unless you omit the body entirely); tools like rebase can get confused if you run the two together.
- Always leave the second line blank.
- Write your commit message in the imperative: "Fix bug" and not "Fixed bug" or "Fixes bug." This convention matches up with commit messages generated by commands like git merge and git revert.
- Further paragraphs come after blank lines.
    - Bullet points are okay, too
    - Typically a hyphen or asterisk is used for the bullet, preceded by a single space, with blank lines in between, but conventions vary here
    - Use a hanging indent

### Commit template

```
[Capitalized, short (50 chars or less) summary]

[More detailed explanatory text, if necessary. Wrap it to about 72 characters]

Link: [GitHub Issue]
```

## IDE

For all development tasks, we prefer:
- [JetBrains](https://www.jetbrains.com/) IDE (IntelliJ IDEA, WebStorm, PyCharm, etc.)
- [Visual Studio Code](https://code.visualstudio.com/) editor

## Semantic versioning

We are using [Semantic Versioning](https://semver.org/) for ILM platform.
