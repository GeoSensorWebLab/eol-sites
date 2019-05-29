# EOL Sites

This is a repository of static web pages to replace web apps no longer supported by GeoSensorWeb Lab. These apps are no longer actively maintained and we want to discontinue maintenance and security updates so our developer has time for other projects.

I chose to use a simple git repository with static assets instead of separate git repositories for Docker/dokku as the latter includes *significant* disk space bloat due to images/containers.

## Usage

The `conf` directory contains nginx configuration files for each static EOL site. These are for virtual host matching.

The `sites` directory contains sub-directories for each EOL site's pages. Each sub-directory should have an `index.html` and associated images, CSS, and JS (although it should be kept to a minimum).

## Deployment

Clone the repository to a web server under the `/var/www` directory. This directory is chosen as it is hard-coded in the site configuration files. Next add a line to your nginx main configuration file to include all configuration files in `/var/www/eol-sites/conf`, and restart the server.

## License

Copyright GeoSensorWeb Lab 2019, All Rights Reserved.
