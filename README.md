# Documentando comandos do Docker para facilitar sua vida :)

### Parando todos os containers do Docker
```sh
$ docker stop $(docker ps -a -q)
$ docker rm $(docker ps -a -q)
```

### Parar todos os containers em execução
```sh
$ docker stop $(docker ps -q | paste -sd " " -)
```

### Parar e remover todos os containers
```sh
$ docker rm -f $(docker ps -aq | paste -sd " " -)
```

### Parar e remover todas as imagens
```sh
$ docker rmi -f $(docker images -aq | paste -sd " " -)
```