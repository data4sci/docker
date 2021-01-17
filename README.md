# containers

<https://www.youtube.com/watch?v=7-7p6WuDtbs>


stažení kontejneru
`# docker pull alpine`

spuštění kontejneru
`# docker run -t -d name mujkontejner alpine`

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
