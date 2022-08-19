# LOAF [Loaf Offers Advanced Functionality] - VVV Bedrock Site Template

This boilerplate is to be used for new projects at Äventyret within the ambition of WP standardization.

## Requirements

- [VVV (varyingvagrantvagrants)](https://varyingvagrantvagrants.org)
- [Node](https://nodejs.org/en/) – the version specified in `./nvmrc`, preferably installed with [nvm](https://github.com/nvm-sh/nvm)
- [Yarn](https://yarnpkg.com/)

## About VVV

VVV is an open source local development environment focused on WordPress, powered by Vagrant.

## Setup a new project in VVV
1. Add site to your config/config.yml

```
project-name:
  hosts:
    - project-name.test
```

2. Reprovision with `vagrant reload --provision`

## Installing Sage with Composer

From your WordPress themes directory, run:

```sh
$ composer create-project roots/sage your-theme-name
```

### Running the first build

Run yarn from the theme directory to install dependencies
Update bud.config.js with your local dev URL
Compile assets with yarn build

## Install theme dependencies and build assets

```sh
$ cd public_html/web/app/themes/project-name
$ nvm use # Makes sure you use the node version specified in .nvmrc (if you use nvm)
$ yarn && yarn build
```

### Access:

Access the website: `https://project-name.test`

Access WordPress admin: `https://project-name.test/wp/wp-admin/`

Access files:

```sh
$ vagrant ssh
$ cd /srv/www/project-name
```

## Run locally

Start vm:

```sh
$ vagrant up
```

## Connect to DB

vvv.test/3306/external/external

## Local development

Build theme assets with hot reload using Yarn:

```sh
$ cd public_html/web/app/themes/project-name
$ nvm use # Makes sure you use the node version specified in .nvmrc (if you use nvm)
$ yarn start
```

