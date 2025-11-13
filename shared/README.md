# Shared containers

Here the setup is done for containers that are shared resources for other containers.

## TSDProxy

I put [TSDProxy](https://almeidapaulopt.github.io/tsdproxy/) here, which allows for every container to join the tailscale network by adding a few label lines to each seperate container that should join, for example:

```yaml
    labels:
      tsdproxy.enable: true
      tsdproxy.name: "pwndrop"
      tsdproxy.funnel: true # Make available outside of network
```

You shouldn't add the `tsdproxy.funnel` option to each container unless you want to expose them all to the big bad world.

## Redis

In this set-up [Redis](https://redis.io/) is quite useless (and you can remove it without affecting the setup), but when you combine them with Nextcloud or some other apps you can gain app performance.

## Databases

The Immich compose file uses a database container, but because no there are no other services using the same database backend engine I left it there. If you have multiple apps using the same database backend engines you could consider making one shared instance in this docker compose instead of spinning up a database engine for each seperately, reducing the memory footprint.
