# Clean up front-end deploy packages

Every time the front-end is deployed a new zip archive is pushed to disk on Azure (see [this task, section 2.1](../../../sprint-1/technical-tasks/2-front-end/1-expanding-the-cicd-pipeline/4-build-a-cd-pipeline.md)). This will fill-up the disk over time.

You will need to tackle the growing disk usage, especially if your apps [share an App Service Pan](../../../../reference/azure/app-service-plan.md).

As long as your app is running you can clean-up the previous deploys via SSH. This is cumbersome and hard to do (especially on the acceptance app).

Can you think of an automated solution to fix this?

