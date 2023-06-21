#SSL

Генерация server.key и server.crt
openssl req -new -text -passout pass:abcd -subj /CN=localhost -out server.req -keyout privkey.pem
openssl rsa -in privkey.pem -passin pass:abcd -out server.key
openssl req -x509 -in server.req -text -key server.key -out server.crt
chmod 600 server.key

Запуск
docker run -d --name postgres -e POSTGRES_HOST_AUTH_METHOD=trust -v "$(pwd)/server.crt:/var/lib/postgresql/server.crt:ro" -v "$(pwd)/server.key:/var/lib/postgresql/server.key:ro" postgres:12-alpine -c ssl=on -c ssl_cert_file=/var/lib/postgresql/server.crt -c ssl_key_file=/var/lib/postgresql/server.key
