# Home Assistant Add-on: Mosquitto & Tailscale

[![Release][release-shield]][release] ![Project Stage][project-stage-shield] ![Project Maintenance][maintenance-shield]

## About

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


[maintenance-shield]: https://img.shields.io/maintenance/yes/2023.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[release-shield]: https://img.shields.io/badge/version-v0.1.2-blue.svg
[release]: https://github.com/elcajon-tech/addon-mosquitto-tailscale/tree/v0.1.2
[mosquitto]: https://mosquitto.org
[mosquitto-ha]: https://github.com/home-assistant/addons/tree/master/mosquitto