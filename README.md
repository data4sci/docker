# containers

<https://www.youtube.com/watch?v=7-7p6WuDtbs>

[15 Docker Commands You Should Know | by Jeff Hale | Towards Data Science](https://towardsdatascience.com/15-docker-commands-you-should-know-970ea5203421)


* A **Docker image** either *exists* or it doesn’t.
* A **Docker container** either *exists* or it doesn’t.
* A **Docker container** that exists is either *running* or it isn’t.


## install docker

[Install Docker and Docker Compose on Linux Mint 19 | ComputingForGeeks](https://computingforgeeks.com/install-docker-and-docker-compose-on-linux-mint-19/)

[Run the Docker daemon as a non-root user (Rootless mode) | Docker Documentation](https://docs.docker.com/engine/security/rootless/)

```bash
sudo apt-get -y  install docker-ce docker-compose
sudo usermod -aG docker $USER
#reboot!
```

## basic commands

stažení kontejneru
`# docker pull alpine`

výpis docker images
`docker images`

vytvoření kontejneru (minimal Linux distro Alpine)
`# docker create muj-alpine-kontejner alpine`

spuštění kontejneru
`# docker run -t -d --name mujkontejner alpine`

stopnutí kontejneru
`# docker my-container stop`

výpis běžících kontejnerů
`# docker ps`

otevřít bash v kontejneru
`# docker exec -it mujkontejner /bin/bash`

kopie kontejneru
`# docker cp <file> <container_id>:/path/to/copy`

přepínače
`sudo docker run -d -p 8888:8888 --name jupyter jupyter/scipy-notebook`
* `-d` detach - spusť na pozadí
* `-p 8888:8888` Publish a container's port(s) to the host
* `--name jupyter` Assign a name to the container

## docker compose
```bash
docker-compose up -d
```
