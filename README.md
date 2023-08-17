# Role spreadcat.openpgp

Ansible role for manging a local openpgp instance on a host.

## Requirements

* The role requires `gathered_facts: true` to be set.

## Role Variables

```yaml
opengpg_default_key: str
```

* Sets the key id for the default key to be used.

```yaml
openpgp_public_keys: list
```

* List of public keys to import from a keyserver.

## Other Variables

```yaml
openpgp_agent_config_file_path: str
```

* Sets the default file path for the GPG agent.

```yaml
openpgp_agent_config_file_source: str
```

* Set the default template for gpg-agent configuration.

```yaml
openpgp_config_file_path: str
```

* Sets the default location for the configuration file.

```yaml
openpgp_config_file_source: str
```

* Default template for the gpg configuration.

```yaml
openpgp_group: str
```

* Default group for all files.

```yaml
openpgp_owner: str
```

* Sets the default owner for all files.

## Dependencies

* None

## Example Playbook

```yaml
---
- hosts: all
  gather_facts: true
  become: true
  role:
    - role: spreadcat.openpgp
```

## License

* BSD

## Author Information

* This role is written an maintained by DBV.
