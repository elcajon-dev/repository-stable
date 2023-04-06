# Home Assistant Add-ons

![Project Stage][project-stage-shield]
![Maintenance][maintenance-shield]
[![License][license-shield]](LICENSE.md)


## About

Home Assistant allows anyone to create add-on repositories to share their
add-ons for Home Assistant easily. This repository is one of those repositories,
providing extra Home Assistant add-ons for your installation.

## Installation

Use the following button to quickly add the repository:

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Felcajon-tech%2Frepository-stable)

Or use the following URL to add this repository:

```txt
https://github.com/elcajon-tech/repository-stable
```

## Add-ons provided by this repository

### &#10003; [Advanced Code Server][addon-code-server]

![Latest Version][code-server-version-shield]
![Supports armhf Architecture][code-server-armhf-shield]
![Supports armv7 Architecture][code-server-armv7-shield]
![Supports aarch64 Architecture][code-server-aarch64-shield]
![Supports amd64 Architecture][code-server-amd64-shield]
![Supports i386 Architecture][code-server-i386-shield]

Code Server experience integrated in the Home Assistant frontend.

[:books: Advanced Code Server add-on documentation][addon-doc-code-server]

### &#10003; [Mosquitto & Tailscale][addon-mosquitto-tailscale]

![Latest Version][mosquitto-tailscale-version-shield]
![Supports armhf Architecture][mosquitto-tailscale-armhf-shield]
![Supports armv7 Architecture][mosquitto-tailscale-armv7-shield]
![Supports aarch64 Architecture][mosquitto-tailscale-aarch64-shield]
![Supports amd64 Architecture][mosquitto-tailscale-amd64-shield]
![Supports i386 Architecture][mosquitto-tailscale-i386-shield]

Open source MQTT broker combined with zero config VPN

[:books: Mosquitto & Tailscale add-on documentation][addon-doc-mosquitto-tailscale]

### &#10003; [Tailscale][addon-tailscale]

![Latest Version][tailscale-version-shield]
![Supports armhf Architecture][tailscale-armhf-shield]
![Supports armv7 Architecture][tailscale-armv7-shield]
![Supports aarch64 Architecture][tailscale-aarch64-shield]
![Supports amd64 Architecture][tailscale-amd64-shield]
![Supports i386 Architecture][tailscale-i386-shield]

Zero config VPN for building secure networks

[:books: Tailscale add-on documentation][addon-doc-tailscale]

## Releases

Releases are based on [Semantic Versioning][semver], and use the format
of ``MAJOR.MINOR.PATCH``. In a nutshell, the version will be incremented
based on the following:

- ``MAJOR``: Incompatible or major changes.
- ``MINOR``: Backwards-compatible new features and enhancements.
- ``PATCH``: Backwards-compatible bugfixes and package updates.

## Support

Got questions?

- [Open an issue for the add-on: Advanced Code Server][code-server-issue]
- [Open an issue for the add-on: Mosquitto & Tailscale][mosquitto-tailscale-issue]
- [Open an issue for the add-on: Tailscale][tailscale-issue]

For a general repository issue or add-on ideas [open an issue here][issue]

## License

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[addon-code-server]: https://github.com/elcajon-tech/addon-code-server/tree/v0.5.1
[addon-doc-code-server]: https://github.com/elcajon-tech/addon-code-server/blob/v0.5.1/README.md
[code-server-issue]: https://github.com/elcajon-tech/addon-code-server/issues
[code-server-version-shield]: https://img.shields.io/badge/version-v0.5.1-blue.svg
[code-server-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[code-server-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[code-server-armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[code-server-armv7-shield]: https://img.shields.io/badge/armv7-no-red.svg
[code-server-i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[addon-mosquitto-tailscale]: https://github.com/elcajon-tech/addon-mosquitto-tailscale/tree/v0.2.3
[addon-doc-mosquitto-tailscale]: https://github.com/elcajon-tech/addon-mosquitto-tailscale/blob/v0.2.3/README.md
[mosquitto-tailscale-issue]: https://github.com/elcajon-tech/addon-mosquitto-tailscale/issues
[mosquitto-tailscale-version-shield]: https://img.shields.io/badge/version-v0.2.3-blue.svg
[mosquitto-tailscale-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[mosquitto-tailscale-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[mosquitto-tailscale-armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[mosquitto-tailscale-armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[mosquitto-tailscale-i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[addon-tailscale]: https://github.com/elcajon-tech/addon-tailscale/tree/v0.6.5
[addon-doc-tailscale]: https://github.com/elcajon-tech/addon-tailscale/blob/v0.6.5/README.md
[tailscale-issue]: https://github.com/elcajon-tech/addon-tailscale/issues
[tailscale-version-shield]: https://img.shields.io/badge/version-v0.6.5-blue.svg
[tailscale-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[tailscale-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[tailscale-armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[tailscale-armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[tailscale-i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[issue]: https://github.com/elcajon-tech/repository-stable/issues
[license-shield]: https://img.shields.io/github/license/elcajon-tech/repository-stable.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2023.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[semver]: http://semver.org/spec/v2.0.0.html