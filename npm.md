version: '3'
services:
  app:
    image: 'chishin/nginx-proxy-manager-zh:release'
    restart: always
    ports:
      - ‘880:80'
      - ‘881:81'
      - ‘8443:443'
    volumes:
      - ./data:/data
      - ./letsencrypt:/etc/letsencrypt
