A `docker-compose.yml` to get [Commento](https://commento.io) and [Traefik](https://traefik.io) with automatic Let's Encrypt certs up and running quickly and painless.

1. Install Docker and Docker Compose
2. Prepare a Docker volume for your Postgres DB and Traefik config files
3. Edit `docker-compose.yml` and change strings in `{}` with your configuration
4. Create the internal docker network
4. `docker-compose up -d`
5. Enjoy a great commenting system!

Hints:
- Set `COMMENTO_FORBID_NEW_OWNERS: "true"` to `"false"` the first time you start up and create your admin user. Then, shut the stack down and change it back to `"true"`. Unless you want to allow everyone to register and add their own domains/sites.
- If you want to run the containers locally, you might want to change ports, too.

Based on:
- https://github.com/acheremisov/ghost-commento-traefik-in-docker
- https://docs.traefik.io/v2.0/user-guides/docker-compose/acme-http/
- https://docs.commento.io/installation/self-hosting/on-your-server/docker.html

