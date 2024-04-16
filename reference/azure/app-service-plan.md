# App Service Plan

An app service always runs in an App Service plan. An App Service plan defines a set of compute resources for a web app to run.

When you create an App Service plan in a certain region (for example, West Europe), a set of compute resources is created for that plan in that region. Whatever apps you put into this App Service plan run on these compute resources as defined by your App Service plan.

**Notice that apps that share an app resource plan also share resources.**

More information can be found on this links:

* https://learn.microsoft.com/en-us/azure/app-service/overview-hosting-plans
* https://learn.microsoft.com/en-us/azure/app-service/app-service-plan-manage

## App Service Plan & Disk Usage

Most of our apps will run in an App Service Plan of the free tier. A free App Service Plan comes with 1GB of storage.

It is in your best interest to define each app in a separate App Service Plan so that every app has 1GB of storage. If apps share the same App Service Plan, they also share the same storage.

If all apps are on a different plan but storage is still not sufficient, you can scale-up one of your plans to a paying tier using your credit.
