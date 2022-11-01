# Docker Java

Para compilação e entrega de projetos escritos em Java

Veja mais em [hub.docker.com/r/tmvdl/java](https://hub.docker.com/r/tmvdl/java)

## Como usar

Instalar o [Docker](https://docs.docker.com/engine/install/).

### Em ambiente de desenvolvimento (opção 1)

Criar um arquivo `docker-compose.yaml` na raiz do projeto com a imagem [tmvdl/java](https://hub.docker.com/r/tmvdl/java):

```yaml
version: '3'

services:
  app:
    image: tmvdl/java
    volumes:
      - .:/app
```

Subir o container para a construção do build:

```bash
docker-compose up --build
```

### Em ambiente de desenvolvimento (opção 2)

Executar os seguintes comando:

```bash
bash env/run.sh maven
```

### Em ambiente de produção

Executar com container do Docker:

```sh
docker run tmvdl/java
```

## License

[MIT](./LICENSE)
