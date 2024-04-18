# Acceptance Environment

Currently you have 2 environments:

* Every developer has a develop-environment on their local machine
* There is a production-environment on Azure

This should change to the following:

* Every developer has a develop-environment on their local machine
* There is an acceptance-environment on Azure where the work of all team-members comes together and can be validated
* There is a production-environment on Azure that runs a stable version of the application for demo purposes

The acceptance environment should be a new web app on Azure. Take note of [these constraints](../../../../reference/azure/app-service-plan.md) regarding App Service Plans and compute resources.

Ideally, the CI pipeline publishes the build artifact to the acceptance environment automatically after publishing to GitHub Packages. However, if there is no [automatic clean-up of old front-end deploys](./../priority-2/clean-up-front-end-deploy-packages.md), then this will not be feasible due to disk space constraints. In that case you can make the deploy to acceptance a separate manual deploy.

The deploy pipeline should remain as is, with a manual deploy from GitHub Packages to production.