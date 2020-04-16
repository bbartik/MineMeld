# MineMeld
Docker Compose file for MineMeld

This is a quick and easy way to create a MineMeld container with docker-compose.

For MineMeld's TLS keypair, you can use the example certificates in the `examples/certs/` directory, or create your own certificates. If you create your own keypair, copy your 
certificates to the `local/certs/` directory. Cerficates must be nammed `server.key` and `server.crt`.

By default, MineMeld will run on port 4433. You can change MineMeld's port in the `docker-compose.yml` file if desired.

Enter `docker-compose up -d` and access MineMeld  on the Docker host via https://yourhost:4433

Login with the username and password of admin and minemeld. Once logged in, you can use the example configuration file, `example/minemeld-config.yml`. If you
would like to add a custom prototype, place it in the `local/prototypes` directory. There is an example prototype for Covid-19 related fraud in `examples/covid19-fraud.yml`.


