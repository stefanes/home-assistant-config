# Home Assistant config

Available Home Assistant configuration snippets:

- [`z_wave_multicast.yaml`](packages/z_wave_multicast.yaml) - package for handling Z-Wave multicasting.
- [`z_wave_errors.yaml`](packages/z_wave_errors.yaml) - package for catching and coming back from various Z-Wave errors.
- [`unresponsive_switches.yaml`](packages/unresponsive_switches.yaml) - sometimes switches does not toggle, undetected by Home Assistant, so I use this setup to detect when that happens.
- [`tibber_nordpool.yaml`](packages/tibber_nordpool.yaml) - package for the [Tibber](https://www.home-assistant.io/integrations/tibber)/[Nord Pool](https://github.com/custom-components/nordpool) integrations. See also the dashboard example [here](lovelace/tibber_nordpool.yaml), using [ApexCharts Card](https://github.com/RomRider/apexcharts-card) to display price info.
- [`trafiklab.yaml`](packages/trafiklab.yaml) - package for setting up sensors for buses/trains in Sweden, as supported by [Trafiklab](https://www.trafiklab.se/api/). See also the dashboard example [here](lovelace/trafiklab.yaml), using [Mushroom Cards](https://github.com/piitaya/lovelace-mushroom) to display departure times.

## Packages

My configuration is mostly split into [packages](https://www.home-assistant.io/docs/configuration/packages/) - place the `.yaml` files in `/config/packages` and add this to `configuration.yaml`:

```yaml
homeassistant:
  ...
  packages: !include_dir_named packages
```
