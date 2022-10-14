# traefik-plugin-dev

1. Run whoam in docker container

```console
$ docker run -d -P --name iamfoo traefik/whoami
# grab port from next line and use in traefik config
$ docker inspect --format '{{ .NetworkSettings.Ports }}'  iamfoo
```

2. Run traefik with config file

```console
traefik --configfile traefik.yaml
```

3. curl localhost:8000/whoami
   See request-id header
