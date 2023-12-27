# Usa a imagem oficial do Python no Docker Hub como imagem base
FROM python:latest

# Define o diretório de trabalho como /app/backend
WORKDIR /app/backend/core

# Copia apenas os arquivos pyproject.toml e poetry.lock para aproveitar o processo de construção PEP 517 do Poetry
COPY ./app/backend/core/pyproject.toml ./app/backend/core/poetry.lock ./

# Instala o Poetry e as dependências do projeto
RUN pip install --no-cache-dir poetry && \
    poetry config virtualenvs.create false && \
    poetry install --no-interaction --no-ansi

# Copia o conteúdo do diretório local /app/backend para o contêiner em /app/backend
COPY ./app/backend /app/backend

# Expõe a porta 5000 para o host
EXPOSE 80

# Comando executado ao iniciar o contêiner
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "80"]
