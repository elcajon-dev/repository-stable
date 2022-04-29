# Home Assistant Add-on: Code Server

Code Server experience integrated in the Home Assistant frontend,
allowing you to edit your Home Assistant configuration directly from your
web browser.

The add-on has the Home Assistant, MDI icons and YAML extensions pre-installed
and pre-configured right out of the box. This means that auto-completion works
instantly, without the need for configuring anything.

## Installation

The installation of this add-on is pretty straightforward and not different in
comparison to installing any other Home Assistant add-on.

1. Add the repository
1. Install the add-on
1. Start the add-on
1. Click the "OPEN WEB UI" button to open Visual Studio Code.

## Custom Init scripts

When `init_path` configuration option is set. The add-on will generate
the two folders `cont-init.d` and `services.d`.

Place your custom cont-init and services files inside the folder and
they will be processed during add-on startup phase.

## SSH service

Assign a port to activate the SSH service.
The service config file (`/etc/ssh/sshd_config`) is saved persistent and can
be adapted to fit your needs.
Public keys can be put inside `/root/.ssh/authorized_keys`and will be saved
persistent as well.

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

### Option: `init_path`

The `init_path` option allows to set the path containing the custom
init scripts and services. For exmpale `/share` will lead to
`/share/code-server/{cont-init.d,services.d}`.

If this option isn't set, this function will not work.

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

## Resetting your Code Server settings to the add-on defaults

The add-on updates your settings to be optimized for use with Home Assistant.
As soon as you change a setting, the add-on will stop doing that since it
might be destructive. However, in case you changed some things, but want to
return to the defaults as delivered by this add-on, do the following:

1. Open the Visual Studio Code editor.
1. Click on `Terminal` in the top menu bar and clik on `New Terminal`.
1. Execute the following command in the terminal window: `reset-settings`.
1. Done!
