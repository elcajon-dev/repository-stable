# Home Assistant Add-on: Nextcloud

This add-on provides Nextcloud for Home Assistant.

- MariaDB is required as database for Nextcloud to work
- Nextcloud configuration data will kept persistent under `/data/nextcloud`
- Nextcloud user data will kept persistent under `/data/nextcloud_data`

## Installation

The installation of this add-on is pretty straightforward and not different in
comparison to installing any other Home Assistant add-on.

1. Install MariaDB add-on as prerequisite for Nextcloud add-On to work
1. Add the repository to your configuration.
1. Search for the "Nextcloud" add-on in the Supervisor add-on store and install it.
1. Start the "Nextcloud" add-on.
1. Check the logs of the "Nextcloud" add-on to see when initialization is done.
1. Open `<ip>:8080` to create an admin user.

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

Nextcloud add-on configuration:

```yaml
reset_database: true|false
trusted_domains:
  - 192.168.0.5
  - nextcloud.example.com
```

### Option: `reset_database`

The `reset_database` option lets you reset (drop and create again)
the Nextcloud database.

Please note that only the database will be purged and no configuration
or user data will be affected by this operation.

### Option: `trusted_domains`

The `trusted_domains` option lets you add domains which will
be accepted to access nextcloud.

Please note that the first domain/ip will be added automatically.

## Use Nginx proxy to secure instance (enable https)

1. Install Nginx Proxy Manager add-on (follow add-on guide)
1. Create a virtual host with your (sub)domain and issue a Letsencrypt certificate
1. Add the code below to the virtual host `advanced` tab.
1. Add the (sub)domain to `trusted_domains`

```conf

location ^~ /.well-known {
    # The following 6 rules are borrowed from `.htaccess`

    location = /.well-known/carddav     { return 301 /remote.php/dav/; }
    location = /.well-known/caldav      { return 301 /remote.php/dav/; }
    # Anything else is dynamically handled by Nextcloud
    location ^~ /.well-known            { return 301 /index.php$uri; }

    try_files $uri $uri/ =404;
}

```

## Changelog & Releases

This repository keeps a change log using [GitHub's releases][releases]
functionality.

Releases are based on [Semantic Versioning][semver], and use the format
of `MAJOR.MINOR.PATCH`. In a nutshell, the version will be incremented
based on the following:

- `MAJOR`: Incompatible or major changes.
- `MINOR`: Backwards-compatible new features and enhancements.
- `PATCH`: Backwards-compatible bugfixes and package updates.

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

[releases]: https://github.com/elcajon/addon-nextcloud/releases
[semver]: http://semver.org/spec/v2.0.0.html
