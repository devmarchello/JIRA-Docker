sudo mkdir -p /opt/jira/activate
sudo nano /opt/jira/docker-compose.yaml
mkdir -p /opt/jira/nginx/certs
sudo nano /opt/jira/nginx/nginx.conf
cd /opt/jira/nginx
openssl req -x509 -nodes -days 365 -newkey rsa:2048  -keyout certs/selfsigned.key  -out certs/selfsigned.crt  -subj "/C=RU/ST=Moscow/L=My/O=ITZM/OU=TECH/CN=jira.domain.local"
cd /opt/jira/
docker-compose up -d

