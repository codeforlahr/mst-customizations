# MST lahr.codes customizations

This repository contains customizations and scripts which can be loaded ontop of the generic MST website.
The customizations adapt the templates to display information specific to our MST instance.
Furthermore the scripts and docker files are stored here for an easier redeployment of the system.


## Setup (WIP)
First clone this repository.
To install the lahr.codes version of MST, follow the instructions of the [generic meine-stadt-transparent instructions](https://github.com/meine-stadt-transparent/meine-stadt-transparent/#production-setup-with-docker-compose), but consider following differences:

### Adapted Docker configuration files
For various files referenced in that instruction, already adapted versions exist in this repository.
This includes the:
 * `docker-compose.yml`
 * `.env.template`

### Template customizations
Customizations to the templates are already included in `/customizations`. The modified `docker-compose.yml` mounts that folder into the container.

### Secrets
The secrets are stored in the `.env`. All fields, marked with `changeme` have to be filled in.
In the future, we could look into using [Docker secrets](https://docs.docker.com/engine/swarm/secrets/#about-secrets). But first issue #2 has to be fixed.
