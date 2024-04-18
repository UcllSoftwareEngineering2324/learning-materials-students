# Schema Management

Currently every environment manages its database schema through JPA.

This should change to the following:

* The development-environment schema is generated with JPA
* The integration tests schema is generated with JPA
* The acceptance-environment schema is written manually using SQL
* The production environment schema is written manually using SQL

The schema of acceptance and production should be automatically updated when a new version reaches these environments.

Think of the following scenario:

* Application version "A" is running on acceptance and production. Both databases have a schema that accommodates version "A".
* Application version "B" supersedes version "A" and needs a new schema.
* When application version "B" is pushed to acceptance, that schema needs to be updated. The production environment should still be running on a schema for version "A".
* When application version "B" is pushed to production, all environments should be using the new database schema.

It is not a good idea to manually update the schemas every time a new version is released. 

Look at tools like "Flyway" (best in combination with Spring Boot, not with maven) to automate this on startup of the application.
