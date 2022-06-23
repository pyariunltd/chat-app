FROM nginx:latest

RUN rm /etc/nginx/conf.d/*

COPY ./nginx.conf /etc/nginx/conf.d/nginx.conf

COPY ./proxy_params /etc/nginx/proxy_params

COPY ./index.html ./index.html

