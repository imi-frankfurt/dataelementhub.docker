# DataElementHub Docker

DataElementHub is based on the fundamental concepts of the [Samply.MDR](https://bitbucket.org/medicalinformatics/mig.samply.mdr.gui).
Based on the experience gained, the concept was revised and redeveloped, with particular emphasis on
the separation of the backend and frontend.
DataElementHub is the next evolution of [MIG.MDR](https://github.com/mig-frankfurt/mdr.gui), introducing
a rebranding.

Please see the [DataElementHub](https://dataelementhub.de/) website for further information.

## Deployment

This project gives you an exemplary setup of DataElementHub in docker containers. The ports are **not**
mapped to the host ports, so you have to set up a reverse proxy in order to use it properly.
If you use this setup, the gui will be available at http://your.network.prefix.4:3000 - feel free to
change these values as you see fit.

You will also need an OAuth Provider - e.g. Keycloak - in order to run DataElementHub. Setting it
up is not part of this README.

1. Download the files in this project to your workdir
2. Modify the .env file and the init.sql file with matching values for the db name, db user name and db user password
3. Call `docker-compose up -d` and wait for it to start
4. Configure your reverse proxy accordingly