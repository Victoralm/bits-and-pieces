# Setup traefik

[traefik docs](https://doc.traefik.io/traefik/)

Basic setup of traefik proxy.

Created a standard Docker network, `frontend`, to serve as the main network for all web apps:

```bash
docker network rm <old-network-name> # Remove a previous netwot, if needed
docker network create frontend
docker network ls # To check the actual existing networks
```

On docker compose file, make sure that Docker will not overrite the network with:

```docker-compose
...

networks:
    frontend:
        external: true
```

Create rules for each desired container, like:

```docker-compose
labels:
    - traefik.http.routers.almsNginx2.rule=Host(`nx2.localhost`)
```
