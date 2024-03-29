# Documentando comandos do Docker para facilitar sua vida :)

![Docker, se você não usa...você está pra trás...](https://gifimage.net/wp-content/uploads/2018/11/docker-gif-4.gif)

### Parando todos os containers do Docker
```sh
$ docker stop $(docker ps -a -q)
$ docker rm $(docker ps -a -q)
```

### Construir e executar imagem
```sh
$ docker-compose up
```
### Construir e executar imagem em segundo plano
```sh
$ docker-compose up -d
```
### Parar um container que esteja em execução
```sh
$ docker stop id-container
```
### Parar todos os containers em execução
```sh
$ docker stop $(docker ps -q | paste -sd " " -)
```

### Para remover um único container
```sh
$ docker container rm <container ID>
```

### Para deletar múltiplos containers
```sh
$ docker container rm <container ID> <container ID>
```

### Parar e remover todos os containers
```sh
$ docker rm -f $(docker ps -aq | paste -sd " " -)
```

### Parar e remover todas as imagens
```sh
$ docker rmi -f $(docker images -aq | paste -sd " " -)
```
### Remover uma imagem específica
```sh
$ docker rmi IMAGE_ID -f
```
### Criar imagem e subir no docker hub
```sh
docker build -t joaovictorbarreto/rubywd .
```
```sh
docker login
```
```sh
docker push joaovictorbarreto/rubywd
```

### Executar um container em segundo plano
```sh
docker container run -d <container ID>
```

### Start e Restart Docker
```sh
killall Docker && open /Applications/Docker.app
```

### Comandos Docker
[Comandos Docker](https://stack.desenvolvedor.expert/appendix/docker/comandos.html)




