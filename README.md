# Home Assistant config

Available Home Assistant configuration snippets:

- `packages/z-wave.yaml` - package for handling Z-Wave devices, including catching and coming back from various errors.

## Packages

My configuration is mostly split into [packages](https://www.home-assistant.io/docs/configuration/packages/), in `configuration.yaml`:

```yaml
homeassistant:
  ...
  packages: !include_dir_named packages
```
