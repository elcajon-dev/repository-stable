# Home Assistant Add-on: Generic

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

Generic Home Assistant add-on.

## About

This is an development add-on for Home Assistant.

It creates initial s6-supervisor file structure within the /share folder:

- /share/addon-generic/cont-init.d - for init scripts
- /share/addon-generic/services.d - for init of services

File structures will be created on first start of the add-on.
If no service files are present in services.d folder, the add-on will stop.

After changing any files simply restart the add-on.

[:books: Read the full add-on documentation][docs]

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
[commits-shield]: https://img.shields.io/github/commit-activity/y/elcajon/addon-generic.svg
[commits]: https://github.com/elcajon/addon-generic/commits/main
[contributors]: https://github.com/elcajon/addon-generic/graphs/contributors
[docs]: https://github.com/elcajon/addon-generic/blob/main/generic/DOCS.md
[github-actions-shield]: https://github.com/elcajon/addon-generic/workflows/CI/badge.svg
[github-actions]: https://github.com/elcajon/addon-generic/actions
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[issue]: https://github.com/elcajon/addon-generic/issues
[license-shield]: https://img.shields.io/github/license/elcajon/addon-generic.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2022.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[releases-shield]: https://img.shields.io/github/release/elcajon/addon-generic.svg
[releases]: https://github.com/elcajon/addon-generic/releases
[repository]: https://github.com/hassio-addons/repository
