# Home Assistant Add-on: Cloudflared Tunnel

[![GitHub Release][releases-shield]][releases]
![Project Stage][project-stage-shield]
[![License][license-shield]](LICENSE.md)

![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports i386 Architecture][i386-shield]

[![Github Actions][github-actions-shield]][github-actions]
![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

Cloudflared Tunnel Home Assistant add-on.

## About

This add-on provides a Cloudflare Tunnel making it possible connecting
to your Home Assistant instance without forwarding/opening
any local router ports.

An [Cloudflare][cloudflare] account is needed with your domain
correctly configured.

## Configuration

1. Start the add-on
1. Check the logs and open the displayed URL to link your cloudflare account.
1. Cloudflared Tunnel `homeassistant` will be configured automatically.
1. [Ingress Routing][ingress-route] can be done inside the
   file `/share/cloudflared/config.yaml`. Make sure to adjust `hostname`
   to the domain or subdomain you use for Home Assistant
1. Add DNS `CNAME` for every configured hostname within
   `/share/cloudflared/config.yaml`, check the logs for `CNAME` destination
   URL.
1. Restart add-on to propagate changes to the Cloudflare Tunnel.

## License

MIT License

Copyright (c) 2017-2022 Elcajon

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

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[commits-shield]: https://img.shields.io/github/commit-activity/y/elcajon/addon-cloudflared.svg
[commits]: https://github.com/elcajon/addon-cloudflared/commits/main
[contributors]: https://github.com/elcajon/addon-cloudflared/graphs/contributors
[docs]: https://github.com/elcajon/addon-cloudflared/blob/main/cloudflared/DOCS.md
[github-actions-shield]: https://github.com/elcajon/addon-cloudflared/workflows/CI/badge.svg
[github-actions]: https://github.com/elcajon/addon-cloudflared/actions
[i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[issue]: https://github.com/elcajon/addon-cloudflared/issues
[license-shield]: https://img.shields.io/github/license/elcajon/addon-cloudflared.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2022.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[releases-shield]: https://img.shields.io/github/release/elcajon/addon-cloudflared.svg
[releases]: https://github.com/elcajon/addon-cloudflared/releases
[cloudflare]: https://cloudflare.com
[ingress-route]: https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/configuration/configuration-file/ingress
