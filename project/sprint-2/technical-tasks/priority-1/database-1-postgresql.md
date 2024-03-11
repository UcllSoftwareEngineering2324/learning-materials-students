# PostgreSQL Database

Currently every version of the application uses H2 as a database.

This should change to the following:

* The development-environment backend uses H2
* The integration tests backend run on H2
* The acceptance-environment backend uses an acceptance schema in a dedicated PostgreSQL database
* The production environment backend uses a production schema in a dedicated PostgreSQL database

Use "Azure Database for PostgreSQL" to set-up a PostgreSQL database. Make sure to create the database via Azure For Students so you can profit from a free PostgreSQL database:

* Go to the Azure for Students homepage
* Click on "Explore All" under Free Services
* Click on "Create" under Azure Database for PostgreSQL
* The cost overview should show that you have a large number of free compute hours before you will incur costs
* Make sure that you select the cheapest development configuration, or your free compute hours and your free credit will not suffice for the database costs
