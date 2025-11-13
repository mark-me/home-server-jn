# Pwndrop

Self-deployable file hosting service for sending out red teaming payloads or securely sharing your private files over HTTP and WebDAV.

[Website](https://github.com/kgretzky/pwndrop)

Note how in the docker-compose file the option `funnel` is set to `true`, to enable sharing with devices/users that are not part of your tailscale VPN:

```yaml
    labels:
      tsdproxy.enable: true
      tsdproxy.name: "pwndrop"
      tsdproxy.funnel: true # Make available outside of network
```
