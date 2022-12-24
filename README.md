# ESPHome

I started to experiment with [ESPHome][esphome] as an alternative to [Tasmota][tasmota].

Despite its use of YAML, ESPHome is great and has taken over all my devices. This repository is keeping stuff organized.

## Structure

- 📁 `common`, reusable bits
- 📁 `templates`, reusable templates (define specific type of devices)
- 📁 `scripts`, some utilities (e.g. the continuous integration tests)
- `.secrets.yaml`, a stub file describing the secrets needed by all devices
- `device.*.yaml`, individual device definitions (define specific instances of devices)

## Secrets

All secrets needed by the configuration is defined in the stub `.secrets.yaml` file.

Because of how ESPHome implements the [`!secret` directive][secret], it is only available at the root of this repository (i.e. in individual device definitions).

<!-- References: -->
[esphome]: https://esphome.io/
[tasmota]: https://tasmota.github.io/docs/
[secret]: https://esphome.io/guides/faq.html?highlight=secret