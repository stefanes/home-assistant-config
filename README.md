# Home Assistant config

Available Home Assistant configuration snippets:

- `packages/z-wave-multicast.yaml` - package for handling Z-Wave multicasting.
- `packages/z-wave-errors.yaml` - package for catching and coming back from various Z-Wave errors.
- `packages/unresponsive-switches.yaml` - sometimes switches does not toggle, undetected by Home Assistant, so I use this setup to detect when that happens.
- `packages/tibber-nordpool.yaml` - package for the [Tibber](https://www.home-assistant.io/integrations/tibber)/[Nord Pool](https://github.com/custom-components/nordpool) integrations.

## Packages

My configuration is mostly split into [packages](https://www.home-assistant.io/docs/configuration/packages/), in `configuration.yaml`:

```yaml
homeassistant:
  ...
  packages: !include_dir_named packages
```
