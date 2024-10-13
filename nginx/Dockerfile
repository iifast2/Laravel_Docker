# /Users/medaminebentaieb/Docker_files/laravel_docker_image/nginx/Dockerfile

FROM nginx:latest

# Install Supervisord
RUN apt-get update && apt-get install -y supervisor

# Copy Nginx configuration files
COPY conf.d/ /etc/nginx/conf.d/

# Copy Supervisord configuration
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# Expose ports
EXPOSE 80 443

# Start Supervisord
CMD ["/usr/bin/supervisord"]
