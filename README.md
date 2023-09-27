# moodle BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

- after the docker installation follow these [instructions](INSTALL-APP.md)

## Standalone Installation 

Clone the github repository. If necessary change the ports in the environment file `.env` and the volume mounts in `docker-compose.yml`.

```
git clone https://github.com/bibbox/app-moodle
cd app-moodle
docker-compose up -d
```

The main app can be opened and set up at
```
http://localhost:80
```

## Install within BIBBOX

Visit the BIBBOX page and find the App by its name in the Store. Click on the symbol and select Install. Then fill the parameters below and name your app click install again.

## Docker Images used
  - [bitnami/mariadb](https://hub.docker.com/r/bitnami/mariadb) 
  - [bitnami/moodle](https://hub.docker.com/r/bitnami/moodle) 


 
## Install Environment Variables
  - USER = Username for admin moodle user
  - PASSWORD = Password for the admin moodle user
  - DB_USER_PASSWORD = User Password for DB User bn_moodle
  - DB_ADMIN_PASSWORD = Admin Password, please change for production

  
The default values for the standalone installation are:
  - USER = user
  - PASSWORD = bitnami
  - DB_USER_PASSWORD = bibbox
  - DB_ADMIN_PASSWORD = bibbox

  
## Mounted Volumes
### bitnami/mariadb Conatiner
  - *./data/mariadb_data/:/bitnami/mariadb/*
### bitnami/moodle Conatiner
  - *./data/moodle_data:/bitnami/moodle*
  - *./data/moodledata_data:/bitnami/moodledata*
