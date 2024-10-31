# Ready-to-go kata bootstrap projects

This repository contains starter projects for running katas in a variety of languages. All projects are using the latest language and framework versions (thanks to [renovate](https://github.com/renovatebot/)) and run on any device straight out of the box using Visual Studio Code and [devcontainers](https://code.visualstudio.com/docs/remote/containers). 


<b>In the cloud:</b> Select the language from below and click "Open in GitHub Codespace" or "Open in GitPod"

<b>In VisualStudio Code:</b> Select the language from below and click "Open in VisualStudio Code"

<b>In IntelliJ:</b> [Click here to clone this repository in IntelliJ](https://rradczewski.github.io/kata-bootstraps/redirect.html?url=jetbrains%3A%2F%2Fidea%2Fcheckout%2Fgit%3Fidea.required.plugins.id%3DGit4Idea%26checkout.repo%3Dhttps%253A%252F%252Fgitlab.com%252Fwith-humans%252Fdevops-workshop%252Finfrastructure.git%26checkout.repo%3Dhttps%253A%252F%252Fgithub.com%252Frradczewski%252Fkata-bootstraps.git) (requires [Jetbrains Toolbox](https://www.jetbrains.com/lp/toolbox/)) and select your language either by opening one of the subfolders as a project or by switching the branch.

| Language  | Resources | Test Command | Quick Start |
|---|---|---|---|
| <p align="center"><a alt="C# Dotnet" href="./csharp"><img width="100px" src="csharp/csharp-original.svg" /><br/>C# Dotnet</a></p> | [C# Reference](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/)<br/>[Dotnet Reference](https://learn.microsoft.com/en-us/dotnet/api/)<br/>[Fluent Assertions](https://fluentassertions.com/introduction) | `dotnet test` | <p><a href="https://github.com/codespaces/new?hide_repo_select=true&repo=rradczewski%2Fkata-bootstraps&ref=csharp">☁️ Open in GitHub Codespace</a></p>  <p><a href="https://gitpod.io/#https://github.com/rradczewski/kata-bootstraps/tree/csharp">☁️ Open in GitPod</a></p>  <p><a href="https://rradczewski.github.io/kata-bootstraps/redirect.html?url=vscode%3A%2F%2Fvscode.git%2Fclone%3Furl%3Dhttps%253A%252F%252Fgithub.com%252Frradczewski%252Fkata-bootstraps.git%26ref%3Dcsharp">💻 Open in VSCode</a></p>

## Contributing a bootstrap

The general paradigm of this repository is to create self-contained, minimal starter projects that are least likely to (silently) break in the future and can automatically be kept up-to-date.

Any bootstrap project may be added to this repository, if:

- The language is not yet present **or** the test-framework enables a different paradigm than the bootstraps already present for the language (e.g. a cucumber or mutation testing tool, not just junit4 or testng)
- Dependencies and docker images are well-known and commonly used
    - Avoids using custom Dockerfile-based dev-containers (they will have to be built each time a devcontainer starts)
    - Uses only one testing framework and one assertion library
- One failing, and one succeeding test exists
- Version numbers are fixed (so they can be picked up and updated by renovate)

A bootstrap needs to contain a valid [`.devcontainer.json`](./java/.devcontainer/devcontainer.json) that configures a container with all appropriate tooling. See any of the existing bootstrap projects for reference.

## Other kata bootstraps

- [swkBerlin/kata-bootstraps](https://github.com/swkberlin/kata-bootstraps) - A huge collection of kata-bootstraps in plenty of languages with plenty of different frameworks
