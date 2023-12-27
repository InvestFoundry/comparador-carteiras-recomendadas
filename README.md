# Comparador de Carteiras

Comparador de Desempenho de Carteiras de Investimentos

## Descrição

Este projeto visa criar um comparador de desempenho entre carteiras de investimentos, permitindo investidores comparar o desempenho das carteiras recomendadas de casas de análise. 

O aplicativo permitirá aos usuários visualizar e comparar o desempenho de diferentes carteiras recomendadas entre elas, e também com carteiras personalizadas criadas pelo usuário.

## Tecnologias Utilizadas

- **Backend:**
  - FastAPI (Python)
  - SQLAlchemy (ORM para PostgreSQL)
  - PyMongo (Interação com MongoDB)

- **Frontend:**
  - React.js
  - Nginx

- **Banco de Dados:**
  - PostgreSQL (Dados de Mercado)
  - MongoDB (Carteiras Recomendadas)

- **Orquestração de Contêineres:**
  - Docker Compose

## Ambiente de Desenvolvimento

- **VSCode com dev-containers:**
  - Configuração do ambiente de desenvolvimento dentro de contêineres para garantir consistência.

- **WSL (Windows Subsystem for Linux):**
  - Utilizado para ambiente de desenvolvimento.

## Estrutura do Projeto

```
/app
  /frontend
    ... (arquivos do frontend)
  /backend
    ... (arquivos do backend)
  /db
    ... (arquivos de configuração do banco de dados)
```

## Como Contribuir

1. Faça um fork do repositório.
2. Crie uma branch para o desenvolvimento de uma nova feature ou correção de bugs.
3. Desenvolva e faça commits na sua branch.
4. Abra um pull request para revisão.

### Configuração do Ambiente de Desenvolvimento

Este projeto utiliza contêineres Docker para facilitar o desenvolvimento em um ambiente consistente. Siga os passos abaixo para configurar e iniciar o ambiente de desenvolvimento.

#### Pré-Requisitos

Certifique-se de ter as seguintes ferramentas instaladas em seu sistema:

1. **Docker:**
   - Siga as instruções de instalação para o seu sistema operacional [aqui](https://docs.docker.com/get-docker/).
   - Para instalar apenas o docker engine, siga as instruções [aqui](https://docs.docker.com/engine/install/)
    > OBS: Caso queria utilizar o docker-engine no WSL2, [esse guia](http://https://github.com/codeedu/wsl2-docker-quickstart) explica como instalar e configurar o docker.

2. **Docker Compose:**
   - Siga as instruções de instalação para o seu sistema operacional [aqui](https://docs.docker.com/compose/install/).

3. **VSCode com dev-containers:**
   - Instale o VSCode em [https://code.visualstudio.com/](https://code.visualstudio.com/).
   - Adicione a extensão "Remote - Containers" ao VSCode.

#### Iniciando o Ambiente de Desenvolvimento

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/InvestFoundry/comparador-carteiras-recomendadas.git
   cd comparador-carteiras-recomendadas
    ```

2. **Construa os containers:**

    ```bash
    docker compose build
    ```

3. **Inicie os Serviços:**

    ```bash
    docker compose up -d
    ```

**Observações**

- Certifique-se de que as portas 5000 e 3000 estejam disponíveis em seu sistema.
- Ao fazer alterações nos arquivos, o hot-reload estará ativado tanto para o backend quanto para o frontend, facilitando o desenvolvimento.

## Licença

Este projeto é licenciado sob a [Licença Apache 2.0](LICENSE).
