FROM node:latest

COPY ./ .

RUN npm install
RUN npm run build

FROM ubuntu:focal

RUN apt-get update
RUN apt-get install -y nginx
RUN rm /var/www/html/index.nginx-debian.html

RUN sed -i -r "s/=404/\/index.html/g" /etc/nginx/sites-enabled/default

WORKDIR /var/www/html

COPY --from=0 ./dist/. .


# Append "daemon off;" to the beginning of the configuration
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80

# Set the default command to execute
# when creating a new container
CMD service nginx start