# MineMeld
Docker Compose file for MineMeld

This is a quick and easy way to create a MineMeld container with docker-compose.

To get started create the directories needed for the MineMeld volumes:
```mkdir -p minemeld/local minemeld/certs minemeld/prototypes```


For MineMeld's TLS keypair, you can use the example certificates in the `examples/certs/` directory, or create your own certificates. Either way, copy your 
certificates to the `local/certs/` directory. Cerficates must be nammed `server.key` and `server.crt`. You can create a self-signed certificate with this command:
```openssl req -x509 -newkey rsa:2048 -nodes -keyout conf.d/server.key -out conf.d/server.crt -days 365```

Enter `docker-compose up -d` and access MineMeld  on the Docker host via https://yourhost

Login with the username and password of admin and minemeld. Once logged in, you can use the example configuration file, `example/minemeld-config.yml`. If you
would like to add a custom prototype, place it in the `local/prototypes` directory. There is an example prototype for Covid-19 related fraud in `examples/covid19-fraud.yml`.


