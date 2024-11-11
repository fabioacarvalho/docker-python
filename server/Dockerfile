FROM nginx:1.21.3-alpine

# Apagando a configuracao padrao
RUN rm /etc/nginx/conf.d/default.conf

# Copiando a nova configuracao para o local padrao
COPY nginx.conf /etc/nginx/conf.d