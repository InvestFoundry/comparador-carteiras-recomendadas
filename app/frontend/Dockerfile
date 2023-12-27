# Utiliza uma imagem Nginx leve como imagem base
FROM nginx:alpine

# Remove a configuração padrão do Nginx
RUN rm -rf /etc/nginx/conf.d/*

# Copia os arquivos de build do React.js para o diretório web root do Nginx
COPY build /usr/share/nginx/html

# Expõe a porta 80 para o host
EXPOSE 80

# Comando para executar quando o contêiner é iniciado
CMD ["nginx", "-g", "daemon off;"]
