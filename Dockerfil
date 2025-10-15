# Use the official nginx image to serve static files
FROM nginx:stable-alpine

# Remove default nginx static content
RUN rm -rf /usr/share/nginx/html/*

# Copy site files to nginx html directory
# Make sure your index.html and all assets (image folder, css, js) are in the build context (repo root)
COPY . /usr/share/nginx/html

# Expose nginx port
EXPOSE 80

# Use the default nginx entrypoint/cmd
# If you'd like custom nginx config, add it to ./nginx.conf and COPY it to /etc/nginx/conf.d/default.conf
