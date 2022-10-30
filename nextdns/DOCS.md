# Home Assistant Add-on: NextDNS Router

This add-on sets up NextDNS router CLI for your local network.

## Prerequisites

In order to use this add-on, you'll need a NextDNS account.

It is free to use for personal & hobby projects, up to 300.000 requests/month
on a single user account.

<https://https://my.nextdns.io>

## Installation

1. Click the Home Assistant My button below to open the add-on on your Home
   Assistant instance.

   [![Add Repository to HA][my-ha-badge]][my-ha-url]

1. Click the "Install" button to install the add-on.
1. Start the "NextDNS" add-on.
1. Check the logs of the "NextDNS" add-on to see if
   everything went well.
1. Done!

## Configuration

```yaml
subnet_config:
  - 192.168.0.0/24=abc123
  - 192.168.1.0/24=def456
default_config: ghi789
log_level: info
```

### Option: `default_config`

This option specifies the default NextDNS config ID.
This configuration is used if no other `subnot_config` fits your device network.

### Option: `subnet_config`

This option allows you to specify different NextDNS configurations for different
parts of your network.

For example:

```yaml
subnet_config:
  - 192.168.0.0/24=abc123
  - 192.168.1.0/24=def456
```

### Option: `nextdns_log`

If set to true, all DNS queries will be printed to the add-on log.

This option specifies the default NextDNS config ID.
This configuration is used if no other `subnot_config` fits your device network.

### Option: `log_level`

The `log_level` option controls the level of log output by the addon and can
be changed to be more or less verbose, which might be useful when you are
dealing with an unknown issue. Possible values are:

- `trace`: Show every detail, like all called internal functions.
- `debug`: Shows detailed debug information.
- `info`: Normal (usually) interesting events.
- `warning`: Exceptional occurrences that are not errors.
- `error`: Runtime errors that do not require immediate action.
- `fatal`: Something went terribly wrong. Add-on becomes unusable.

Please note that each level automatically includes log messages from a
more severe level, e.g., `debug` also shows `info` messages. By default,
the `log_level` is set to `info`, which is the recommended setting unless
you are troubleshooting.

[my-ha-badge]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[my-ha-url]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Felcajon-tech%2Frepository-stable
