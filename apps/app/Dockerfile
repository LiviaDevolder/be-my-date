# Use a imagem base Node.js
FROM node:alpine

# Instale pnpm globalmente
RUN npm install -g pnpm

# Defina o diretório de trabalho
WORKDIR /app

# Copie o package.json e o pnpm-lock.yaml
COPY package.json pnpm-lock.yaml ./

# Instale as dependências
RUN pnpm install

# Copie o restante do código da aplicação
COPY . .

# Build da aplicação, se necessário
RUN pnpm run build

# Exponha a porta que a aplicação irá rodar
EXPOSE 3000

# Comando para rodar a aplicação
CMD ["pnpm", "start"]
