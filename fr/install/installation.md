## Installation  ##
---

Rejoignez-nous sur le chat à l'adresse [https://gitter.im/claroline/Claroline](https://gitter.im/claroline/Claroline).

This repository fournit la structure de base de l'application de la plateforme Claroline Connect. It doesn't contain the sources nor the third-party libraries required to make the application fully functional. Those sources have to be installed following one of the procedures described below.

If you want to contribute or directly browse the sources of the project, check the claroline/Distribution repository, which gathers the standard modules and plugins of the platform.
Requirements

L'installation de la version de développement nécessite au minimum:

    PHP >= 5.6 avec les extensions suivantes:
        curl
        fileinfo
        gd
        intl
        mbstring
        mcrypt
        xml
        json
        zip
        ffmpeg (optional)
    MySQL/MariaDB >=5.0
    composer (recent version)
    node.js >= 5.5, <6.0
    npm >= 3.7

Il est vivement recommandé de développer dans un environnement de type Unix.

Pour mysql >= 5.7, il y a une étape supplémentaire:

    mysql -u**** -p
    set global sql_mode='';
    exit;

Installation

1. Depuis une archive pré-construite

Un fichier compressé contenant tout ce qui est nécessaire pour le développement et les tests (pre-fetched sources, database dump, etc.) est disponible à chaque release de la platforme à packages.claroline.net/releases. C'est le moyen le plus rapide pour démarrer:

curl packages.claroline.net/releases/latest/claroline-16.05.tar.gz | tar xzv
cd claroline-16.05
php scripts/configure.php
composer fast-install

2. From source

The raw installation procedure is comprised of several steps that need to be executed in order (fetching php sources, installing dev dependencies, building, creating the database, etc.). Except for the configuration step, the whole process is managed through composer scripts listed in the composer.json file. For an installation from scratch, the commands would be:

git clone http://github.com/claroline/Claroline
cd Claroline
php scripts/configure.php
composer sync-dev

3. From web installer

curl packages.claroline.net/releases/latest/claroline-16.05.tar.gz | tar xzv

Open /install.php from your webserver and follow the instructions.
Upgrade

To update an existing development installation, just pull the latest changes (or a specific version) of this repository and use the sync-dev script:

git pull
composer sync-dev

Development

Some assets of the platform are managed by webpack. In a development environment, they require the webpack dev server to be running. You can start it with:

npm run watch

Obviously, you'll also need a PHP-enabled web server to serve the application. Two alternatives are available.
1. Using PHP's built-in web server

This is the simplest and recommended way of serving the application during development. To start the server, use the command provided by the symfony framework (more details here):

php app/console server:start

The application will be available at http://localhost:8000.

2. Using a standalone web server

If you want to use Apache or Nginx during development, make them serve the web directory, and access the application at http://localhost/example-site/app_dev.php.

Note that you'll certainly face permissions issues on the following directories:

    app/cache
    app/config
    app/logs
    app/sessions
    files
    web/uploads

All of them must be recursively writable from both the web server and the CLI. For more information on that subject, see the configuration section of the official Symfony documentation.
Usage

You can create a first admin user with:

php app/console claroline:user:create -a

Plugins

Plugins are managed by composer like any other package in the platform. You can install or uninstall the sources of a plugin by adding or removing the package from the require section of your composer.json and running composer update, or using shortcuts like composer require ....

Once the plugin package is in your vendor directory, you can proceed to the (un-)installation using one the following commands:

php app/console claroline:plugin:install FooBarBundle
php app/console claroline:plugin:uninstall FooBarBundle

Important: Note that the installation and upgrade procedures of the platform described above apply only to the "standard" distribution, which comes with a fixed set of plugins. If you deviate from that set, you'll have to maintain your own composer files and perform composer update and php app/console claroline:update accordingly.
Browser support

We recommend to use Claroline Connect with the latest version of Mozila Firefox or Chromium.

We support :

    Mozilla Firefox (latest version)
    Chromium (latest version) and Google Chrome (latest version)
    Microsoft Edge (latest version)
    Microsoft Internet Explorer 11
    Safari (latest version)

For complete list : http://caniuse.com/#feat=mutationobserver
Documentation

La documentation est disponible à l'adresse http://doc.claroline.com .

For development documentation, see Claroline/CoreBundle/Resources/doc/index.md.