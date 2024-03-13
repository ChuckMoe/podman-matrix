# Config

- Change the passwords in `postgres/init.sql`
- Change the secrets and domain for:
	- `coturn.conf`
	- `server.yaml`
	- `bridges/doublepuppet.yaml`
	- `bridges/NAME/config.yaml`

# Installation

```bash
podman pod play kube turn.yaml
podman pod play kube server.yaml
# For every bridge
podman stop matrix-bridge-NAME && podman start matrix-bridge-NAME
```

Now you are good to go, to register the bridges in the server. Register the `doublepuppet.yaml` in the admin channel. Now copy the `registration.yaml` files that were generated.

# Links

- https://gitlab.com/famedly/conduit/-/blob/next/APPSERVICES.md
- https://docs.mau.fi/bridges/index.html