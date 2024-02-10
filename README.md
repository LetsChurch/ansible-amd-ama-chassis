# AMD Advanced Media Acceleration Chassis

This role sets up a chassis for AMD Advanced Media Acceleration as documented here: https://amd.github.io/ama-sdk/v1.0/getting_started_on_prem.html#chassis-setup

All in all, it Enables IOMMU, updates GRUB, and allocates hugepages according to how many devices are installed.

## Requirements

This role is designed to work with Ubuntu. You will need to set `become` as `sudo` is required.

## Role Variables

### `ama_devices`

The number of AMD AMA devices that are installed. Defaults to `1`.

### `hugepages_per_ama_device`

The number of hugepages to allocate per device. Defaults to 2048.

### `additional_hugepages`

The number of additional hugepages to allocate. Defaults to 96.

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: ama-chassis
  roles:
    - role: letschurch.ama-chassis
      ama_devices: 1
```

## License

UNLICENSE
