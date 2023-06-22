# docker-compose-tests-initial
Installation and test docker compose with a CRUD application using php, html, css, and mysql technologies.

To install docker, follow the tutorial on the official docker page at this link https://docs.docker.com/desktop/install/ubuntu/

After having cloned this project, you can check the folder structure

```
.
├── db
│   ├── crud.sql
│   └── Dockerfile
├── docker-compose.yml
├── README.md
└── website
     ├── Dockerfile
     └── www
         ├── config.php
         ├── create.php
         ├── delete.php
         ├── error.php
         ├── index.php
         ├── read.php
         └── update.php
´´´

Being divided into 2 main folders, the db for the bank and the web application with the php code.

As part of docker compose at the root, I have the docker-compose.yml file where you can check all the .yml coding that assembles the containers, volumes and network. In each directory there is the Dockerfile file that will assemble the image or specific command of each container, it is called automatically by compose.

A crud.sql scheme is used to assemble the database, and a volume separated from the container is mounted using the docker compose file, so the database will remain static and there is no danger of losing it when restarting a container, it will only be deleted when deleting the container.

To start the containers with dokcer, just access the root directory of the project via terminal and run the command "docker compose up -d" with this will download the container images and run them, when you finish the process in the browser you can access the application through the url "localhost:8000" or "IP-CONTAINER:80".

You already have a mini application running.

To shut down for a moment use the command "docker compose stop", so it will hang up until you upload the containers again

To completely delete them, use the "docker compose down" command, thus deleting all files except the creation images.