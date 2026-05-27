# Use official nginx image to serve static files
FROM nginx:alpine

# Copy the docs folder to nginx html directory
COPY docs/ /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]