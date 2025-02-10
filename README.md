# devops-reverse-proxy

## Demo

- Create a new network:

```sh
docker network create devops-reverse-proxy
```

- Go to the `app` folder and start the applications:

```sh
cd app && docker compose up -d
```

- Start the reverse proxy - caddy:

```sh
cd caddy && docker compose up -d
```

- Modify `hosts` file:

```
127.0.0.1   it-tools.local.hue-dev.top
127.0.0.1   s.local.hue-dev.top
127.0.0.1   s-ui.local.hue-dev.top
```

- Access:
    - http://it-tools.local.hue-dev.top
    - http://s-ui.local.hue-dev.top
