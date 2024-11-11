# Docker and Python

_Para utilizar esse projeto você precisa ter o [Docker](https://docs.docker.com/desktop/install/windows-install/) instalado e configurado._

Se por acaso estiver utilizando no *__windows__*, você precisará instalar o [WSL](https://learn.microsoft.com/en-us/windows/wsl/install).


_O usuário e senha do postgreSQL será os mesmos que você definiu no arquivo .env_

## Iniciando o porjeto

Para iniciar o projeto basta fazer o __clone__ do repositório, para isso basta rodar o comando.

```
git clone "https://LINK_DO_REPOSITORIO"
```

Feito isso dentro da pasta __db__ crie um arquivo chamado __.env__ e adicionar os seguintes comandos:

``` 
SECRET_KEY="CHANGE-ME"
POSTGRES_DB="CHANGE-ME"
POSTGRES_USER="CHANGE-ME"
POSTGRES_PASSWORD="CHANGE-ME"
```

_Para servir de exemplo tem um arquivo chamado __.env-examplo__ aonde você pode visualizar como fazer seu arquivo .env._

## Executando o projeto

Para executar o projeto basta rodar o comando:

``` 
docker-compose up --build 
```

Se quiser __forçar a recriação__ do container use o comando abaixo:

```
docker-compose up --build --force-recreate
```

## Comandos Extras


- __Criar novos apps:__
```
docker-compose run djangoapp python manage.py startapp nome_do_app
```
Perceba que aqui estamos utilizando o __djangoapp__ na frente do python, isso porque ele se refere ao nome do serviço que criamos dentro do arquivo __docker-compose.yml__.

_Então para executar qualquer comando basta adicionar o __docker-compose run djangoapp__ na frente_.


- __Visualizar os logs:__
```
docker-compose up
```
_Feito isso você poderá ver os __logs__ do sistema no terminal como por exemplo, caso execute um print(''), caso não queira visuarlizar os logs, basta aficionar o __-d__ no final do comando._


- __Visualizar/listar os container:__
```
docker ps -a
```
_Feito isso você pode verificar o __ID__ do container_


- __Visualizar/listar as imagens:__
```
docker image ls
```


_Se por acaso precisar __apagar um container__, você pode usar os seguintes comandos:_

- __Remover um container por ID:__
```
docker rm ID_DO_CONTAIER
```

<br>
