# Home Assistant config

Available Home Assistant configuration snippets:

- [`z_wave_multicast.yaml`](packages/z_wave_multicast.yaml) - package for handling Z-Wave multicasting.
- [`z_wave_errors.yaml`](packages/z_wave_errors.yaml) - package for catching and coming back from various Z-Wave errors.
- [`unresponsive_switches.yaml`](packages/unresponsive_switches.yaml) - sometimes switches does not toggle, undetected by Home Assistant - this setup can be used to detect when that happens.
- [`tibber.yaml`](packages/tibber.yaml), [`nord_pool.yaml`](packages/nord_pool.yaml), and [`electricity_price.yaml`](packages/electricity_price.yaml) - packages for the [Tibber](https://www.home-assistant.io/integrations/tibber) and [Nord Pool](https://www.home-assistant.io/integrations/nordpool) integrations to get electricity price information. See also [dashboard example](dashboards/electricity_price.yaml) (using [ApexCharts Card](https://github.com/RomRider/apexcharts-card) to display price info).
- [`trafiklab.yaml`](packages/trafiklab.yaml) - package for setting up sensors for buses/trains in Sweden, as supported by [Trafiklab](https://www.trafiklab.se/api/). See also [dashboard example](dashboards/trafiklab.yaml) (using [Mushroom Cards](https://github.com/piitaya/lovelace-mushroom) to display departure times).
- [`firmware_update.yaml`](packages/firmware_update.yaml) - package for monitoring firmware updates for various devices.

## Packages

[Packages](https://www.home-assistant.io/docs/configuration/packages/) in Home Assistant provide a way to bundle configurations from multiple integrations - place the `.yaml` files in `/config/packages` and add this to `configuration.yaml`:

```yaml
homeassistant:
  ...
  packages: !include_dir_named packages
```

## Macros

Centrally define your own Jinja2 macros and import and use them anywhere in Home Assistant - place the `.jinja` files in `/config/custom_templates`. More information:

- [Macros for your templates](https://www.home-assistant.io/blog/2023/04/05/release-20234/#macros-for-your-templates)
- [Reusing templates](https://www.home-assistant.io/docs/configuration/templating/#reusing-templates)

## Notes

### Device Id

You can get the `device_id` by navigating to **Settings > Devices & Services > Devices**, selecting the device, and copying the last part of the URL (`.../config/devices/device/[device_id]`).

### Config Entry Id

You can get the `config_entry_id` by navigating to **Settings > Devices & Services > Entities**, selecting one of the entities belonging to the integration, selecting **... > Related > Integration** and copying the last part of the URL (`.../config/integrations/integration/<integration>#config_entry=[config_entry_id]`).
