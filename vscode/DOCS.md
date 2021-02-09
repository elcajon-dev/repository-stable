# Home Assistant Add-on: Visual Studio Code - armv7/aarch64 Version

This add-on runs Visual Studio Code, allowing you to edit your Home Assistant
configuration directly from your web browser and can be embedded straight
into the Home Assistant frontend UI.

Visual Studio Code runs as a remote server using `code-server`, and is a
fully fledged VSCode experience.

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

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

Example add-on configuration:

```yaml
packages:
  - mariadb-client
init_commands:
  - ls -la
```

**Note**: _This is just an example, don't copy and paste it! Create your own!_

### Option: `packages`

Allows you to specify additional [Ubuntu packages][ubuntu-packages] to be
installed in your shell environment (e.g., Python, PHP, Go).

**Note**: _Adding many packages will result in a longer start-up
time for the add-on._

### Option: `init_commands`

Customize your VSCode environment even more with the `init_commands` option.
Add one or more shell commands to the list, and they will be executed every
single time this add-on starts.

## Resetting your VSCode settings to the add-on defaults

The add-on updates your settings to be optimized for use with Home Assistant.
As soon as you change a setting, the add-on will stop doing that since it
might be destructive. However, in case you changed some things, but want to
return to the defaults as delivered by this add-on, do the following:

1. Open the Visual Studio Code editor.
1. Click on `Terminal` in the top menu bar and clik on `New Terminal`.
1. Execute the following command in the terminal window: `reset-settings`.
1. Done!
