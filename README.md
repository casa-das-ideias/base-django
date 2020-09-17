# Docker Django - Postgres - Gunicorn - Nginx

## Usando o projeto para?

### Desenvolvimento

Para usar o servidor padrão de desenvolvimento.

1. Renomeie *.env.dev-exemplo* para *.env.dev*.
1. Atualize as variaveis de ambiente nos arquivos *docker-compose.yml* e *.env.dev*.
1. Crie as imagens e execute os contêineres:

    ```sh
    $ docker-compose up -d --build
    ```

    Teste este endereço no browser [http://localhost:8000](http://localhost:8000). A pasta "app" é montada no contêiner e as alterações de código são aplicadas automaticamente.

### Produção

Usando o gunicorn + nginx.

1. Renomeie *.env.prod-exemplo* para *.env.prod* e *.env.prod.db-exemplo* para *.env.prod.db*. Atualize as variaveis de ambiente.
1. Crie as imagens e execute os contêineres:

    ```sh
    $ docker-compose -f docker-compose.prod.yml up -d --build
    ```

    Teste este endereço [http://localhost:1337](http://localhost:1337). Sem pastas montadas. Para aplicar as alterações, a imagem deve ser reconstruída.

## Gerando Secret Key Para o Projeto:

[djecrety](https://djecrety.ir/)

https://pynative.com/python-generate-random-string/

https://github.com/paul-wolf/strgen

https://youtu.be/-qe66sKk-dQ?t=2873



docker-compose -f docker-compose.staging.yml up -d --build


../console python manage.py createsuperuser

PS: atualizar documentação