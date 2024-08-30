# latest nginx image as base
FROM nginx:latest

# Copy front-end files to Nginx server directory
COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy Nginx configuration file
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf