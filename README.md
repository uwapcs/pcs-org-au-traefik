# pcs-org-au-traefik
Traefik docker-compose config for pcs.org.au

# Setup
- Check you are happy with `.env`
  - The below instructions assume you have `TRAEFIK_PERSISTENT_ROOT=/mnt/persistent/traefik`, modify as required
- Initialize `acme.json`:
  - `mkdir -p /mnt/persistent/traefik` to make the directory
  - `touch /mnt/persistent/traefik/acme.json` to make the file
  - `chmod 600 /mnt/persistent/traefik/acme.json` to set file permissions
- `docker network create web` to create the network for other containers to talk to Traefik
- `docker-compose up -d` to deploy Traefik
