FROM node:20.10.0-alpine3.18

# TODO: Colocar o chown como nobody e nogroup, mudar a permissão dos arquivos,
# colocar os arquivos como propriedade do usuário que será criado
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "server.js"]

# TODO: Criar um usuário não-root para rodar a aplicação de forma mais segura para 
# seguir as melhores práticas de segurança em contêineres.
