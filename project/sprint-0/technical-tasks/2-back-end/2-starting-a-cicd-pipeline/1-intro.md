# Intro

In these tasks we will start building cicd pipelines for the backend. The ultimate goal is that your **default branch (normally "main")** will be build and deployed to Azure every time you push new code.
In this sprint we will only build a small part, we will finish the pipelines in sprint-1.

You are encouraged to go through the reference material so that you have the necessary background knowledge.

## 1. Reference

* [cicd](./../../../../../reference/ci-cd/cicd.md)
    * What is cicd and why is it important?
* GitHub
    * Started out as a part of the git ecosystem but has evolved to a whole build platform tightly integrated with Azure
    * [GitHub the platform](./../../../../../reference/github/github.md); get to know the many faces of GitHub
    * [GitHub Actions](./../../../../../reference/github/github-actions.md); we will use GitHub Actions as a build system
    * [GitHub Packages](./../../../../../reference/github/github-packages.md); we will use GitHub Packages as a storage place for our build artifacts