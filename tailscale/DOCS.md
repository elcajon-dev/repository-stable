# Home Assistant Add-on: Adguard-Tailscale

Tailscale is a zero config VPN, which installs on any device in minutes,
including your Home Assistant instance.

Create a secure network between your servers, computers, and cloud instances.
Even when separated by firewalls or subnets, Tailscale just works. Tailscale
manages firewall rules for you, and works from anywhere you are.

## Prerequisites

In order to use this add-on, you'll need a Tailscale account.

It is free to use for personal & hobby projects, up to 20 clients/devices on a
single user account. Sign up using your Google, Microsoft or GitHub account at
the following URL:

<https://login.tailscale.com/start>

If you want to use the build in proxy server,
make sure to enable HTTPS support for your Tailnet.
This option needs to be enabled in Tailscale DNS settings.

<https://tailscale.com/kb/1153/enabling-https/>

Since Home Assistant blocks requests from proxies/reverse proxies, you need to
tell your instance to allow requests from the Tailscale add-on.
In order to do so, add the following lines to your `/config/configuration.yaml`
without changing anything:

```yaml
http:
  use_x_forwarded_for: true
  trusted_proxies:
    - 127.0.0.1
```

**Note**: _There is no need to adapt anything in these lines since the addon
runs on your host network._

## Installation

1. Click the Home Assistant My button below to add the repository to your Home
   Assistant instance.

   [![Add Repository to HA][my-ha-badge]][my-ha-url]

1. Click the "Install" button to install the add-on.
1. Start the "Tailscale" add-on.
1. Check the logs of the "Tailscale" add-on to see if everything went well.
1. Open the Web UI of the "Tailscale" add-on to complete authentication and
   couple your Home Assistant instance with your Tailscale account.
   **Note:** Some browsers don't work with this step. It is recommended to
   complete this step on a desktop or laptop computer using the Chrome browser.
1. Check the add-on logs to get your Tailscale Home Assistant domain.
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
  - tag:example
  - tag:homeassistant
```

### Option: `tags`

This option allows you to specify specific ACL tags for this Tailscale
instance. They need to start with `tag:`.

More information: <https://tailscale.com/kb/1068/acl-tags/>

### Option: `enable_ssh`

Enable this option to allow clients to connect to your instance via SSH.
The add-on has all configuration folders
(`config`,`backup`,`media`,`share`,`ssl`,`addons`) mapped.

See the Tailscale documentation for further information:

<https://tailscale.com/kb/1193/tailscale-ssh/>

### Option: `enable_exit_node`

Enable this option to advertise this instance as exit node.

### Option: `enable_subnets`

Enable this option to advertise local subnets.

### Option: `enable_funnel`

Enable this option to externally access your instance using your Tailscale
domain. (like `https://homeassistant.furing-otter.ts.net`)

If this option is disabled, you still will be able to access your Home Assistant
instance while locally connected to your Tailscale account.

Check the prerequisites part at the beginning
of this documentation before moving on with the steps below.

Before you can enable the Funnel feature for the addon,
you need to assign the necessary ACL `nodeAttrs`.

Check the following Tailscale guide on how to achieve this:
<https://tailscale.com/kb/1223/tailscale-funnel/#setup>

**Note**: _After initial set up it can take up to 10 minutes for the domain to
be publicly available. You can use the `dig` command (Linux/MacOS) to regulary
check if an A-record is already present for your domain
(`dig homeassistant.YOUR-TS-DOMAIN.ts.net +short` should return an IP address
once the record is published)._

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
[my-ha-url]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Felcajon%2Frepository-stable
