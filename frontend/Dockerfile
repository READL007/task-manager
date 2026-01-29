FROM nginxinc/nginx-unprivileged:alpine3.22-perl@sha256:f1444b4f78f91b0c42dedc01b55972f4d759e7fcbabdf5d5a5e2f0690234eef4

WORKDIR /usr/share/nginx/html
COPY . /usr/share/nginx/html

USER nginx

EXPOSE 5173

HEALTHCHECK --interval=30s --timeout=5s --start-period=5s \
    CMD wget http://localhost/ || exit 1
