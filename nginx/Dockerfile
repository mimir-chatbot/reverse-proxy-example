FROM nginx:1.17.8-alpine

RUN apk update && apk add --no-cache openssl
RUN mkdir -p /etc/nginx/ssl
RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/ssl/nginx.key -out /etc/nginx/ssl/nginx.crt -subj "/C=US/ST=CA/L=San Francisco/O=Global Security/OU=IT Department/CN=example.com"

# Copy the nginx.conf file
COPY default.conf /etc/nginx/conf.d/default.conf

CMD ["nginx", "-g", "daemon off;"]