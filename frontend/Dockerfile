FROM nginxinc/nginx-unprivileged:alpine3.22-perl

WORKDIR /usr/share/nginx/html
COPY . /usr/share/nginx/html

USER nginx

EXPOSE 5173

HEALTHCHECK --interval=30s --timeout=5s --start-period=5s \
    CMD wget http://localhost/ || exit 1
