## What’s changed

# Breaking changes - read carefully before updating!
The folder **/config** has been renamed to **/homeassistant**
The folder **/config** now contains public add-on specific configuration ([click here](https://developers.home-assistant.io/blog/2023/11/06/public-addon-config/) for more information)
The folder **/addon_configs** has been added and contains the add-on specific configuration of all add-ons (which support add-on specific configuration)
The add-on option `init_path` has been removed. Custom scripts can now be placed inside `/config/custom-services`

Create a backup before updating and make sure to adapt custom scripts/services accordingly after the update. 

## 🚨 Breaking changes

- Add support for public add-on configs (/addon_configs) @elcajon (#393)
- Use /config for add-on configuration @elcajon (#395)

## 🐛 Bug fixes

- Bugfix custom-scripts for public add-on configuration @elcajon (#396)

## 🚀 Enhancements

- Add addon_config mapping (/config) @elcajon (#394)

## ⬆️ Dependency updates

- ⬆️ Update frenck/action-addon-linter action to v2.14 @renovate (#392)
