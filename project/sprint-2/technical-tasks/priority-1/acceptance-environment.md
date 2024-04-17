# Acceptance Environment

Currently you have 2 environments:

* Every developer has a develop-environment on their local machine
* There is a production-environment on Azure

This should change to the following:

* Every developer has a develop-environment on their local machine
* There is an acceptance-environment on Azure where the work of all team-members comes together and can be validated
* There is a production-environment on Azure that runs a stable version of the application for demo purposes

The acceptance environment should be a new web app on Azure. Take note of [these constraints](../../../../reference/azure/app-service-plan.md) regarding App Service Plans and compute resources.

The CI pipeline should publish the build artifact to the acceptance environment automatically after publishing to GitHub Packages.

The deploy pipeline should remain as is, with a manual deploy from GitHub Packages to production.