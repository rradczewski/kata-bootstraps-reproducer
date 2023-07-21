# Curated Kata Bootstrap Projects

This repository contains curated starter projects for running katas. All projects are kept up-to-date automatically by [renovate](https://github.com/renovatebot/) and are based on [devcontainers](https://code.visualstudio.com/docs/remote/containers). All languages exist in folders (e.g. `./java`), and branches that are kept in sync through Github Actions.

[Clone repository in IntelliJ](https://rradczewski.github.io/kata-bootstraps/redirect.html?url=jetbrains%3A%2F%2Fidea%2Fcheckout%2Fgit%3Fidea.required.plugins.id%3DGit4Idea%26checkout.repo%3Dhttps%253A%252F%252Fgitlab.com%252Fwith-humans%252Fdevops-workshop%252Finfrastructure.git%26checkout.repo%3Dhttps%253A%252F%252Fgithub.com%252Frradczewski%252Fkata-bootstraps.git) (requires [Jetbrains Toolbox](https://www.jetbrains.com/lp/toolbox/)) and select your language either by opening one of the subfolders as a project or by switching the branch.

|   | Language  | Resources | Test Command | Quick Start |
|---|---|---|---|---|
| <a alt="Haskell" href="./haskell"><img width="100px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/haskell/haskell-original.svg" /></a> | [Haskell](./haskell) |  | `stack test` | [Open in GitHub Codespace](https://github.com/codespaces/new?hide_repo_select=true&repo=rradczewski%2Fkata-bootstraps&ref=haskell)<br/>[Open in GitPod.io](https://gitpod.io/#https://github.com/rradczewski/kata-bootstraps/tree/haskell)<br/>[Open locally in VSCode](https://rradczewski.github.io/kata-bootstraps/redirect.html?url=vscode%3A%2F%2Fvscode.git%2Fclone%3Furl%3Dhttps%253A%252F%252Fgithub.com%252Frradczewski%252Fkata-bootstraps.git%26ref%3Dhaskell)

## Contributing a bootstrap

The general paradigm of this repository is to create self-contained, minimal starter projects that are least likely to (silently) break in the future and can automatically be kept up-to-date.

Any bootstrap project may be added to this repository, if:

- The language is not yet present **or** the test-framework enables a different paradigm than the bootstraps already present for the language (e.g. a cucumber or mutation testing tool, not junit4)
- Dependencies and docker images are well-known and commonly used
    - Avoids using custom Dockerfile-based dev-containers
    - Uses only one testing framework and one assertion library
- One failing, and one succeeding test exists
- Version numbers are either `latest` or [renovate](https://github.com/renovatebot/) can pick them up automatically (e.g. don't use variables in `pom.xml` or elsewhere).

A bootstrap needs to contain a valid [`.devcontainer.json`](./java/.devcontainer/devcontainer.json) that configures a container with all appropriate tooling. Furthermore, the `postCreateCommand` needs to contain a shell command that, when executed, will verify that the test runner correctly runs and reports that two tests ran and one of them failed.

## Other kata bootstraps

- [swkBerlin/kata-bootstraps](https://github.com/swkberlin/kata-bootstraps) - A huge collection of kata-bootstraps in plenty of languages with plenty of different frameworks
