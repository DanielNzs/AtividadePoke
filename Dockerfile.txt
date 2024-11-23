# Use the official Nginx image
FROM nginx:alpine

# Remove the default Nginx page
RUN rm /usr/share/nginx/html/index.html

# Copy custom HTML file to Nginx directory
COPY index.html /usr/share/nginx/html/

# Expose port 80 for HTTP traffic
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
