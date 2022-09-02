# Home Assistant Add-on: Adguard-Tailscale

Tailscale is a zero config VPN, which installs on any device in minutes,
including your Home Assistant instance.

Create a secure network between your servers, computers, and cloud instances.
Even when separated by firewalls or subnets, Tailscale just works. Tailscale
manages firewall rules for you, and works from anywhere you are.

AdGuard Home is a network-wide ad-and-tracker blocking DNS server with parental
control (adult content blocking) capabilities. Its purpose is to let you
control your entire network and all your devices, and it does not require
using a client-side program.

This add-on combines both functionalities and allows you to set up AdGuard
with your Tailscale internal IP. This allows you to block traffic without
forwarding your subnets with Tailscale.

## Prerequisites

In order to use this add-on, you'll need a Tailscale account.

It is free to use for personal & hobby projects, up to 20 clients/devices on a
single user account. Sign up using your Google, Microsoft or GitHub account at
the following URL:

<https://login.tailscale.com/start>

You can also create an account during the add-on installation processes,
however, it is nice to know where you need to go later on.

## Installation

1. 1. **Ensure your Home Assistant device has a
      [static IP and static external DNS servers!](https://github.com/home-assistant/hassos/blob/dev/Documentation/network.md#static-ip)**
      This is important! You **WILL** end up having issues if you skip this step.
1. Click the Home Assistant My button below to open the add-on on your Home
   Assistant instance.

   [![Add Repository to HA][my-ha-badge]][my-ha-url]

1. Click the "Install" button to install the add-on.
1. Start the "Adguard-Tailscale" add-on.
1. Check the logs of the "Adguard-Tailscale" add-on to see if
   everything went well.
1. Check the logs of the "Adguard-Tailscale" add-on to
   complete authentication and
   couple your Home Assistant instance with your Tailscale account.
1. Done!

## Configuration

This add-on has almost no additional configuration options for the
add-on itself.

However, when logging in to Tailscale, you can configure your Tailscale
network right from their interface.

<https://login.tailscale.com/>

The add-on exposes "Exit Node" capabilities that you can enable from your
Tailscale account. Additionally, if the Supervisor managed your network (
which is the default), the add-on will also advertise routes to your
subnet to Tailscale.

```yaml
tags:
  - tag:example-server
  - tag:homeassistant
log_level: info
```

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

### Option: `tags`

This option allows you to specify specific ACL tags for this Tailscale
instance. They need to start with `tag:`.

More information: <https://tailscale.com/kb/1068/acl-tags/>

[my-ha-badge]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[my-ha-url]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Felcajon%2Frepository-stable
