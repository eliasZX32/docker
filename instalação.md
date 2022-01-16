# Ubuntu

Seguir os passos de Instalação, eu usei o link abaixo para instalar

https://docs.docker.com/engine/install/

## use o comando abaixo para desistalar todas instalações antigas

```sudo apt-get remove docker docker-engine docker.io containerd runc```

## Atualizar o repositório 
```sudo apt-get update```

## Instalar o certificado para o uso de um repositório por HTTPS
```sudo apt-get install \ ca-certificates \ curl \ gnupg \ lsb-release```

## Adicione a chave GPG oficial do Docker
```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg```

## Use o comando a seguir para configurar o repositório estável 
```echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \         $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null```

## Atualizar o repositório  
```sudo apt-get update```

## Instalar o docker  
```sudo apt-get install docker-ce docker-ce-cli containerd.io```

## use este comando para pegar a VERSION_STRING
```apt-cache madison docker-ce```

## Instalar a versão do docker-ce, use o comando anterior pra escolher a versão
```sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io```

## Atualizar o repositório  
```sudo apt-get update```
