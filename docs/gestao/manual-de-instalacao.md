# Manual de Instalação do Projeto

## Visão Geral

Este projeto utiliza uma arquitetura de microserviços, composta por quatro repositórios:

1. **Frontend**: Interface do usuário.
2. **Backend - Usuários**: Serviço responsável pelo gerenciamento de usuários.
3. **Backend - Financeiro**: Serviço responsável pelas operações financeiras.
4. **Backend - Benefícios**: Serviço responsável pela gestão de benefícios.

Todos os repositórios são dockerizados, garantindo que os serviços possam ser facilmente configurados e executados.

### Pré-requisitos

Antes de iniciar o processo de instalação, certifique-se de que os seguintes softwares estejam instalados:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Estrutura de Repositórios

- Repositório do [**Frontend**](https://github.com/fga-eps-mds/2024.1-SENTINELA-FRONT)
- Repositório do [**Backend - Usuários**](https://github.com/fga-eps-mds/2024.1-SENTINELA-BACKEND-USUARIOS)
- Repositório do [**Backend - Financeiro**](https://github.com/fga-eps-mds/2024.1-SENTINELA-BACKEND-FINANCEIRO)
- Repositório do [**Backend - Benefícios**](https://github.com/fga-eps-mds/2024.1-SENTINELA-BACKEND-BENEFICIOS)

---

## Passo a Passo de Instalação

### 1. Clonar os Repositórios

Clone os repositórios do projeto em suas respectivas pastas.

```bash
# Clonar o frontend
$ git clone https://github.com/fga-eps-mds/2024.1-SENTINELA-FRONT

# Clonar o backend de usuários
$ git clone https://github.com/fga-eps-mds/2024.1-SENTINELA-BACKEND-USUARIOS

# Clonar o backend de financeiro
$ git clone https://github.com/fga-eps-mds/2024.1-SENTINELA-BACKEND-FINANCEIRO

# Clonar o backend de benefícios
$ git clone https://github.com/fga-eps-mds/2024.1-SENTINELA-BACKEND-BENEFICIOS

```

### 2. Configurar Variáveis de Ambiente

Para cada serviço, crie ou edite o arquivo .env na raiz de cada repositório com as variáveis de ambiente necessárias. Aqui está um exemplo geral para cada serviço:

```
# Exemplo de .env
DB_HOST=db  # Endereço do banco de dados
DB_PORT=5432  # Porta do banco de dados
DB_USER=user  # Usuário do banco de dados
DB_PASSWORD=senha  # Senha do banco de dados
DB_NAME=nome_do_banco  # Nome do banco de dados
PORT=3000  # Porta que o serviço vai rodar
```

Certifique-se de que as variáveis estejam corretamente configuradas em cada microserviço.

### 3. Subir os Containers com Docker

Navegue até a pasta de cada serviço e execute os comandos abaixo para rodar os containers com Docker. Abaixo está o passo a passo para cada serviço:

#### 3.1 Frontend

Entre na pasta do frontend e execute os seguintes comandos:

```
$ cd frontend
$ docker build nome-da-imagem
$ docker run --name nome-do-container -p 5173:5173 nome-da-imagem

```

O frontend estará disponível em: http://localhost:5173 (ou a porta especificada no .env).

#### 3.2 Backend - Usuários

Entre na pasta do backend de usuários e execute:

```bash
$ cd backend-usuarios
$ docker-compose up --build
```

Este serviço estará disponível na porta configurada no .env, como http://localhost:3001.

#### 3.3 Backend - Financeiro

Entre na pasta do backend financeiro e execute:

```bash
$ cd backend-financeiro
$ docker-compose up --build
```

Este serviço estará disponível na porta configurada no .env, como http://localhost:3002.

#### 3.4 Backend - Benefícios

Entre na pasta do backend de benefícios e execute:

```bash
$ cd backend-beneficios
$ docker-compose up --build
```

Este serviço estará disponível na porta configurada no .env, como http://localhost:3003.

## Monitoramento dos Containers

Você pode verificar o status de todos os containers em execução utilizando o comando:

```bash
$ docker ps
```

Caso queira parar todos os serviços, navegue até cada repositório e execute:

```bash
$ docker-compose down --volumes
```

Para remover containers que não estão mais em execução criados pelos docker-compose:

```
$ docker-compose rm -f
```

## Considerações Finais

Com os containers configurados e em execução, a aplicação completa estará disponível para uso. Certifique-se de que todas as portas configuradas estejam livres e que as dependências de rede entre os microserviços estejam funcionando corretamente (como a comunicação entre backends e o banco de dados). Para quaisquer problemas, consulte os logs dos containers com o comando:

```bash
docker logs <nome_do_container>
```

Caso precise recriar os containers, sempre utilize o parâmetro --build ao rodar o docker-compose para garantir que a imagem seja recompilada.

```bash
docker-compose up --build
```

## Histórico de Versões

| Alteração            | Data     | Autor           |
| -------------------- | -------- | --------------- |
| Criação do documento | 08/09/24 | Ingrid Carvalho |
| Revisão              | 08/09/24 | Sara Campos     |
