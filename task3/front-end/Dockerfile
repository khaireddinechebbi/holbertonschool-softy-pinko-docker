# Use the latest version of nginx
FROM docker.io/library/nginx:latest

# Copy the softy-pinko-front-end files to the nginx html directory
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the custom nginx configuration file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
