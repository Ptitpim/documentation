DOCKER
======

- command: `docker version`
  - verified cli can talk to engine
- command: `docker info`
  - most config values of engine
- docker command line structure
  - old (still works): `docker <command> (options)`
  - new: `docker <command> <sub-command> (options)`


Image vs. Container
-------------------

- An Image is the application we want to run
- A Container is an instance of that image running as a process
- You can have many containers running off the same image
- Docker's default image "registry" is called Docker Hub (hub.docker.com)

Exemple :
`docker container run --publish 80:80 nginx`

The Docker engine actually looked for an image called nginx, and it pulled down the latest image for nginx from Docker Hub.
Then it started it as a new process in a new container for us to use.
1. Downloaded image 'nginx' from Docker Hub
2. Started a new container from that image
3. Opened port 80 on the host IP

run vs start
------------

`docker container run` always start a *new container*

Use `docker container start` to start an existing stopped one


Lancer un container en mode détaché
-----------------------------------

Le mode détaché ne bloque pas la console

```bash
docker container run --publish 80:80 --detach nginx
```

Lancer un container avec le nom (unique) : "webhost"
----------------------------------------------------

```bash
docker container run --publish 80:80 --detach --name webhost nginx
```

Lister les container lancés
---------------------------

```bash
docker container ls
```

Lister les container lancés dernièrement et/ou toujours actifs
--------------------------------------------------------------

```bash
docker container ls -a
```

Stopper le container dont on fournit l'ID
-----------------------------------------

```bash
docker container stop <container-id>
```

Lister les process du container
-------------------------------

```bash
docker container top <container-name>
```

Logs
----

```bash
docker container logs
```
old way:

```bash
docker logs
```

show logs for a specific container

user --help to see all the log options

Supprimer (un ou plusieurs containers)
--------------------------------------

```bash
docker container rm
```
old way:
```bash
docker rm
```

Pour supprimer plusieurs container
----------------------------------

```bash
docker container rm <container id> <container id> <container id>
```

On peut par exemple indiquer uniquement les 3 premières lettres/chiffres de l'ID.

On ne peut pas supprimer un container qui est en train de tourner

