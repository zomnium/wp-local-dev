# WordPress Local Development

Having one version of PHP or one database instance on your system is annoying and risky when working on multiple projects. Do you need a different WP or PHP version for one project? Did one project break another? Stop crying and use this Docker template.

By just having a Docker environment per project it makes your life easier, jump around between WP/PHP versions and make adjustments per project with ease. Create a snapshot, trash and/or restore things without touching your other projects.

## What does it include?

- WordPress, you didn't expect that, did you?
- phpMyAdmin for easy moderation of your database
- MariaDB to store your data

## Getting started

1. Make sure you have [Docker installed](https://docs.docker.com/get-docker/) and the daemon is running
2. Clone or download this repo to a new project folder
3. Copy the `example.env` file to `.env` and keep it in your project folder, you can adjust your settings here
4. Run the development environment for the first time with `docker-compose up -d`, it will create the folder structure
5. Move your plugins and themes into the created folders
6. Optionally open phpMyAdmin on http://127.0.0.1:1234 to import your project data
7. Open your project on http://127.0.0.1:8080

## Useful info

- Start the development server as a detached background process: `docker-compose up -d`
- Turn off your development server, when running in the background: `docker-compose down`
- Development server showing all container logs: `docker-compose up`, exit with `ctrl + c`
- You can adjust the WordPress database prefix and debug mode from the env configuration file
- Development server: http://127.0.0.1:8080
- phpMyAdmin: http://127.0.0.1:1234
- MariaDB database: `127.0.0.1:3306`

Note: make sure to run the `docker-compose` commands from within your project directory.

## How to

### Adjust settings

Open up the `.env` file, you can find all the settings there. If you can't find it, copy the `example.env` and rename it to `.env`.

### Switch WordPress or PHP version

This can be done in the `.env` file by switching the tag of the WordPress Docker image, [overview of supported tags](https://hub.docker.com/_/wordpress/).

### Connect to the database with a database manager

You can connect to your IP `127.0.0.1` on port `3306`.
