# LOCAL SETUP DOCKER

## commands list

```bash
docker run -it --rm -v $PWD:/code -v /var/run/docker.sock:/var/run/docker.sock:ro -w /code --name uptime-kuma-development -p 3001:3001 node:20.4 /bin/bash
# inside the container
apt update && apt install -y iputils-ping
npm ci
npm run download-dist
npm run dev
```
