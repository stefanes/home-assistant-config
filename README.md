# Home Assistant config

Available Home Assistant configuration snippets:

- [`z-wave-multicast.yaml`](packages/z-wave-multicast.yaml) - package for handling Z-Wave multicasting.
- [`z-wave-errors.yaml`](packages/z-wave-errors.yaml) - package for catching and coming back from various Z-Wave errors.
- [`unresponsive-switches.yaml`](packages/unresponsive-switches.yaml) - sometimes switches does not toggle, undetected by Home Assistant, so I use this setup to detect when that happens.
- [`tibber-nordpool.yaml`](packages/tibber-nordpool.yaml) - package for the [Tibber](https://www.home-assistant.io/integrations/tibber)/[Nord Pool](https://github.com/custom-components/nordpool) integrations.

## Packages

My configuration is mostly split into [packages](https://www.home-assistant.io/docs/configuration/packages/) - place the `.yaml` files in `/config/packages` and add this to `configuration.yaml`:

```yaml
homeassistant:
  ...
  packages: !include_dir_named packages
```
