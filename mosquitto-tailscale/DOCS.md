# Home Assistant Add-on: Adguard-Tailscale

Eclipse Mosquitto is an open-source (EPL/EDL licensed) message broker that
implements the MQTT protocol. Mosquitto is lightweight and is suitable for use
on all devices from low power single board computers to full servers.
For more information, please see [mosquitto].

Tailscale is a zero config VPN, which installs on any device in minutes,
including your Home Assistant instance.

This add-on allows to publish your Mosquitto server securely with Tailscale.

If you do not plan to access your Mosquitto server from outside your local
server, you can also use the official [Home-Assistand add-on][mosquitto-ha]
to set up your MQTT Mosquitto server.

## Prerequisites

In order to use this add-on, you'll need a Tailscale account.

It is free to use for personal & hobby projects, up to 20 clients/devices on a
single user account. Sign up using your Google, Microsoft or GitHub account at
the following URL:

<https://login.tailscale.com/start>

## Installation

1. Click the Home Assistant My button below to add the repository to your Home
   Assistant instance.

   [![Add Repository to HA][my-ha-badge]][my-ha-url]

1. Click the "Install" button to install the add-on.
1. Check the configuration options and enter your Tailscale auth-key
1. Start the "Mosquitto & Tailscale" add-on.
1. Check the logs of the "Mosquitto & Tailscale" add-on to see
   if everything went well.
1. Home-Assistant will be able out of the box to configure the MQTT integration.
1. You now can also connect to your MQTT server from any Tailscale host.
1. Done!

## Configuration

This add-on has no mandatory configuration options to run, but you want to
add your Tailscale auth-key to use the secured external access to MQTT.

```yaml
tailscale_authkey: "tskey-auth-kSRnfC7CNTRL-xxxxxxxx"
logins:
  - username: user
    password: passwd
```

### Option: `tailscale_authkey`

This option allows you to specify your Tailscale auth-key to connect this
add-on to your tailnet.

More information on how to create auth-keys:

<https://tailscale.com/kb/1085/auth-keys>

### Option: `enable_tailscale_ssh`

Enable this option to allow clients to connect to your instance via SSH.

See the Tailscale documentation for further information:

<https://tailscale.com/kb/1193/tailscale-ssh/>

### Option: `logins`

A list of local users that will be created with username and password.
This option is required if you want to access MQTT from outside the official
[Home-Assistant integration][mosquitto-integration].

```yaml
logins:
  - username: user
    password: passwd
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

[my-ha-badge]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[my-ha-url]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Felcajon%2Frepository-stable
[mosquitto-integration]: https://www.home-assistant.io/integrations/mqtt/
