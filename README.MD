# WordPress On Docker

A simple stack for WordPress development

## What's Included

Official (and latest) images from

- WordPress (which also includes PHP/Apache)
- MariaDB (community fork of MySQL)
- PHPMyAdmin

All that is required (after installing Docker) is to `cd` into the root of this project and run `docker-compose up` or `docker-compose up -d`. This will download the official images, if they aren't already on your local machine, start them up and link them all together. You should then be able to go through the typical WP install by hitting `http://localhost` or where ever your local machine points to.

## Things to note

There will be three volumes created

- one for the database (so db data wont be lost if you run `docker-compose down` or exit the container)
- two for the source - we're not versioning WP core files since the latest core files come with the WP image, so we are just going to version the themes and the plugins directories.