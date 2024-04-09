FROM nginx:1.23-alpine

RUN apk add --no-cache bash


# Remove any existing config files
RUN rm /etc/nginx/conf.d/*

COPY gzip.conf hsts.conf /etc/nginx/includes/
COPY ./default.conf /etc/nginx/conf.d/



# Expose the listening port
EXPOSE 80


# Launch NGINX
CMD [ "nginx", "-g", "daemon off;" ]
