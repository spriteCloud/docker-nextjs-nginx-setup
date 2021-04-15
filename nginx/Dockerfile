# Set nginx base image
FROM nginx:1.19.6-alpine

# Add the server certificates
ADD ./certs/localhost.crt /etc/nginx/ssl/server.crt
ADD ./certs/localhost.key /etc/nginx/ssl/server.key

# Copy custom configuration file from the current directory
COPY nginx.conf /etc/nginx/nginx.conf

COPY maintenance.html /usr/share/nginx/html/

# Expose Nginx HTTP service
EXPOSE 80
EXPOSE 443
