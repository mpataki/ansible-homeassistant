# ansible-homeassistant

[Home Assistant](https://www.home-assistant.io/) is an open source home automation platform. This ansible role manages the various config files for home assistant which has a few benefits. It also provides a playbook for updating home assistant at your leasure.

## Requirements

Really this should work on any debian based system, but has been tested on a Raspberry Pi running Hassbian.

## Role Variables

- `homeassistant_config_dir`: This is the directory on your local machine where you're storing your home assistant config files. The files in the provided directory will be the ones copied to the home assistant host when the role is appled.

Specifically, the following files will be copied from the provided `homeassistant_config_dir`:
- `configuration.yaml`
- `automations.yaml`
- `groups.yaml`
- `customize.yaml`
- `secrets.yaml`
- `scripts` (a directory holding any custom scripts your setup might use)

## Dependencies

None.

## Example Playbook

```yml
    - hosts: pi
      roles:
         - role: mpataki.homeassistant
```

## License

MIT
