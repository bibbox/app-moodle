# Moodle BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/) or standalone. 

* After the docker installation follow these [instructions](INSTALL-APP.md)

## Standalone Installation

Clone the github repsoitory and start the install.sh. If necessary change the ports and volume mounts in `docker-compose.yml`. 

`sudo git clone https://github.com/bibbox/app-varapp`

`sudo chmod +x install.sh`

`sudo ./install.sh`

Default **login** `user`/`bitnami`

You can access varapp via your webbrowser at [http://localhost:80](http://localhost:8080).
Finish your varapp setup by following these [instructions](INSTALL-APP.md).

## Install within BIBBOX

Within BIBBOX you can use the [BIBBOX](https://bibbox.readthedocs.io/en/latest/) to install a lot of software tools. After the installation is finished you can start your application in the dashboard.

Username and password for the **login** is set duringthe installation.

Finish your varapp setup by following these [instructions](INSTALL-APP.md).


## Docker Images Used


 * [bitnami/moodle](https://hub.docker.com/r/bitnami/moodle), Verified Publisher
 * [bitnami/mariadb](https://hub.docker.com/r/bitnami/mariadb), Verified Publisher
 

## Mounted Volumes

- ./data/mariadb_data
- ./data/moodle_data
- ./data/moodledata_data

