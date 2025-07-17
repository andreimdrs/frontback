# Use uma imagem base do Node.js que o Vite 7.0.5 suporte (Node.js 20 é LTS)
FROM node:20-alpine

WORKDIR /app

# Copia os arquivos de configuração do npm para instalar dependências
COPY package.json package-lock.json ./

# Instala as dependências do frontend
RUN npm install

# Copia o restante do código do frontend
COPY . .

# Porta padrão do Vite
EXPOSE 5173 


CMD ["npm", "run", "dev"]