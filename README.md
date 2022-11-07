# WordPress Local Development

Easier not to have your *AMP development environment on global/OS level. Just having it as a Docker container in a project makes it easier to jump between versions and make adjustments per project.

Bonus is everything is scoped to the project, including the db and such. Makes it easier to snapshot, trash and/or restore things without touching other projects.

Apart from having different WP versions, you can also choose your PHP version on project level which can be helpful at times.

## What does it include?

- WordPress, you didn't expect that, did you?
- phpMyAdmin for easy moderation of your database
- MariaDB to store your data

## Getting started

1. Make sure you have Docker and the daemon is running
2. Clone this repo to a new project folder
3. Copy `example.env` to `.env` and keep it in the project folder
4. Run the development environment for the first time with `docker-compose up -d`, it will create the folder structure
5. Move your plugins and themes in the created folders
6. Optionally open phpMyAdmin on http://127.0.0.1:1234 to import your project data
7. Open up your project on http://127.0.0.1:8080

## Useful info:

- Start up development server as a detached background process: `docker-compose up -d`
- Turn off your development server, when running in the background: `docker-compose down`
- Development server showing all container logs: `docker-compose up`, turn it off with `ctrl + c`
- You can adjust the WordPress database prefix and debug mode from the env configuration file
- Development server: http://127.0.0.1:8080
- phpMyAdmin: http://127.0.0.1:1234

Note: make sure to run the `docker-compose` commands from within your project directory.
