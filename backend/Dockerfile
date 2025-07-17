# Use uma imagem base do Python que o FastAPI suporte (Python 3.11 é bom)
FROM python:3.11-slim-buster

WORKDIR /app

# Copia o arquivo de requisitos e instala as dependências
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copia o restante do código do backend
COPY . .

EXPOSE 8000
# Porta padrão do FastAPI

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]