# docker/nginx/Dockerfile
FROM nginx:alpine

# Remove default config
RUN rm /etc/nginx/conf.d/default.conf
# We'll mount our custom config at runtime in docker-compose.yml