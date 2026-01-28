FROM nginx:alpine

WORKDIR /usr/share/nginx/html
COPY . /usr/share/nginx/html

EXPOSE 80

HEALTHCHECK --interval=30s --timeout=5s --start-period=5s \
    CMD wget http://localhost/ || exit 1
