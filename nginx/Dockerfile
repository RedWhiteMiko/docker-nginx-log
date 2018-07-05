# Builds a Docker to deliver dist/
FROM nginx

COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf
COPY dist/ /usr/share/nginx/html

EXPOSE 80
