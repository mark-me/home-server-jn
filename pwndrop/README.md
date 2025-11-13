# pwndrop

Self-deployable file hosting service for sending out red teaming payloads or securely sharing your private files over HTTP and WebDAV.

[Website](https://github.com/kgretzky/pwndrop)

Note how in the docker-compose file the option `funnel` is set to `true`, to enable sharing with devices/users that are not part of your tailscale VPN:

```yaml
    labels:
      tsdproxy.enable: true
      tsdproxy.name: "pwndrop"
      tsdproxy.funnel: true # Make available outside of network
```

Note the setting `SECRET_PATH` for the environment. This sets the subfolder you use when accessing the webclient [https:://pwndrop.tailf786dc.ts.net](https://theuselessweb.com/) like so [https:://pwndrop.tailf786dc.ts.net/pwndrop](https://www.youtube.com/watch?v=E4WlUXrJgy4) to avoid being Rick rolled.

```yaml
      - SECRET_PATH=/pwndrop #optional
```
