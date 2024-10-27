# Imagem base
FROM nginx:alpine

# Copia o arquivo de configuração do Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Copia o frontend para a pasta raiz do container
COPY . /usr/share/nginx/html

# Define a porta do container para o acesso do Nginx
EXPOSE 80