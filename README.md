# Home Assistant Community Add-ons

![Project Stage][project-stage-shield]
![Maintenance][maintenance-shield]
[![License][license-shield]](LICENSE.md)


## About

Home Assistant allows anyone to create add-on repositories to share their
add-ons for Home Assistant easily. This repository is one of those repositories,
providing extra Home Assistant add-ons for your installation.

The primary goal of this project is to provide you (as a Home Assistant user)
with additional, high quality, add-ons that allow you to take your automated
home to the next level.

## Installation

In general, there is no need to install this repository on your
Home Assistant instance. It is activated and added by Home Assistant
by default.

However, if the repository is missing on your setup, adding this add-ons
repository to your Home Assistant instance is pretty easy. In the
Home Assistant add-on store, a possibility to add a repository is provided.

Use the following URL to add this repository:

```txt
https://github.com/elcajon/repository-stable
```

## Add-ons provided by this repository

### &#10003; [Generic][addon-generic]

![Latest Version][generic-version-shield]
![Supports armhf Architecture][generic-armhf-shield]
![Supports armv7 Architecture][generic-armv7-shield]
![Supports aarch64 Architecture][generic-aarch64-shield]
![Supports amd64 Architecture][generic-amd64-shield]
![Supports i386 Architecture][generic-i386-shield]

Generic add-on for development purposes

[:books: Generic add-on documentation][addon-doc-generic]

### &#10003; [Studio Code Server][addon-vscode]

![Latest Version][vscode-version-shield]
![Supports armhf Architecture][vscode-armhf-shield]
![Supports armv7 Architecture][vscode-armv7-shield]
![Supports aarch64 Architecture][vscode-aarch64-shield]
![Supports amd64 Architecture][vscode-amd64-shield]
![Supports i386 Architecture][vscode-i386-shield]

Fully featured VSCode experience, to edit your HA config in the browser, including auto-completion!

[:books: Studio Code Server add-on documentation][addon-doc-vscode]

## Releases

Releases are based on [Semantic Versioning][semver], and use the format
of ``MAJOR.MINOR.PATCH``. In a nutshell, the version will be incremented
based on the following:

- ``MAJOR``: Incompatible or major changes.
- ``MINOR``: Backwards-compatible new features and enhancements.
- ``PATCH``: Backwards-compatible bugfixes and package updates.

## Support

Got questions?

- [Open an issue for the add-on: Generic][generic-issue]
- [Open an issue for the add-on: Studio Code Server][vscode-issue]

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

[addon-generic]: https://github.com/elcajon/addon-generic/tree/v0.0.5
[addon-doc-generic]: https://github.com/elcajon/addon-generic/blob/v0.0.5/README.md
[generic-issue]: https://github.com/elcajon/addon-generic/issues
[generic-version-shield]: https://img.shields.io/badge/version-v0.0.5-blue.svg
[generic-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[generic-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[generic-armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[generic-armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[generic-i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[addon-vscode]: https://github.com/elcajon/addon-vscode/tree/v4.0.3
[addon-doc-vscode]: https://github.com/elcajon/addon-vscode/blob/v4.0.3/README.md
[vscode-issue]: https://github.com/elcajon/addon-vscode/issues
[vscode-version-shield]: https://img.shields.io/badge/version-v4.0.3-blue.svg
[vscode-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[vscode-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[vscode-armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[vscode-armv7-shield]: https://img.shields.io/badge/armv7-no-red.svg
[vscode-i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[awesome-shield]: https://img.shields.io/badge/awesome%3F-yes-brightgreen.svg
[awesome]: https://awesome-ha.com
[discord-shield]: https://img.shields.io/discord/478094546522079232.svg
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg
[gitlabci-shield]: https://gitlab.com/elcajon/repository-stable/badges/master/pipeline.svg
[gitlabci]: https://gitlab.com/elcajon/repository-stable/pipelines
[issue]: https://github.com/elcajon/repository-stable/issues
[license-shield]: https://img.shields.io/github/license/elcajon/repository-stable.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2021.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[semver]: http://semver.org/spec/v2.0.0.html