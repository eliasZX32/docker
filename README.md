# docker

Os principais comandos do Docker

**use o comando abaixo para desistalar todas instalações antigas**

```sudo apt-get remove docker docker-engine docker.io containerd runc```

### Para ver a versão do docker
```docker version```

### contêiners que estão sendo executados
```docker ps``` 

ou 

```docker container ls```

### Mostra os containers que já rotaram
```docker ps -a```

### Para o serviço
```docker stop [contêiner ou id]```

### Logs um contêiner ( abra um novo terminar )
```docker logs [contêiner ou id]```

### Remove um contêiner, ( Cuidado, ele exclui do computador )
```docker rm [contêiner ou id]```
	*-f força parar o contêiner e remove*
	
### Remove uma imagem, ( Cuidado, ele exclui do computador )
```docker rmi [imagem ou id]``` 

### Remove todas imagens, contêiners, redes, cache ( Cuidado )
```docker system prune```

### Mostra algumas informação do contêiner
```docker top [contêiner ou id]```

### Mostra informação gerais do contêiner
```docker inspect [contêiner ou id]```

### Logar e deslogar

```docker login```

```docker logout```

--------------------------
Rodar um contêiner
docker run [opçoes] [imagem]

[opções]
	--detach , -d		Execute o contêiner em segundo plano e imprima o ID do contêiner
 	--expose, -p 8081:80 Expoe a porta 8081, 80 é a porta do contêiner
 	--name novo_nome_contêiner contêiner
 	--rm remove o contêiner após uso, quando voce ter stop o container vai ser apagado
 	
--------------------------

docker run -d -p 8081:80 --name my edyan/php


docker build -t lyubb/docker-mssql-php5 .

