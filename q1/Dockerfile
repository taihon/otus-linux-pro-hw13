FROM alpine:latest
RUN apk update && apk upgrade && apk add nginx && \
    sed -i 's/return 404;/index index.html;\nroot \/var\/www\/localhost\/htdocs;/' /etc/nginx/http.d/default.conf
COPY index.html /var/www/localhost/htdocs/
EXPOSE 80
CMD ["nginx","-g","daemon off;"]