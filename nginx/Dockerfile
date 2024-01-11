FROM nginx:1.17.8-alpine

# Copy the nginx.conf file
COPY default.conf /etc/nginx/conf.d/default.conf

CMD ["nginx", "-g", "daemon off;"]