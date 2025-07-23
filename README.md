1. sudo mkdir -p /opt/jira/activate
2. sudo nano /opt/jira/docker-compose.yaml
3. mkdir -p /opt/jira/nginx/certs
4. sudo nano /opt/jira/nginx/nginx.conf
5. cd /opt/jira/nginx
6. openssl req -x509 -nodes -days 365 -newkey rsa:2048  -keyout certs/selfsigned.key  -out certs/selfsigned.crt  -subj "/C=RU/ST=Moscow/L=My/O=ITZM/OU=TECH/CN=jira.domain.local"
7. cd /opt/jira/
8. docker-compose up -d

