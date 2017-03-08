## Installation

---

Rejoignez-nous sur le chat à l'adresse [https://gitter.im/claroline/Claroline](https://gitter.im/claroline/Claroline).

Ce dépôt fournit la structure de base de l'application de la plateforme Claroline Connect. Il ne contien ni les sources, ni les librairies tierces qui sont nécessaires pour rendre l'application entièrement fonctionnelle. Ces sources doivent être installées en suivant une des procédures décrites ci-dessous.

Si vous désirez contribuer aux sources du projet ou naviguer dedans, rendez-vous au dépôt claroline/Distribution qui rassemble les modules par défaut et les plugins de la plateforme.

### Exigences

L'installation de la version de développement nécessite au minimum:

```
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
```

Il est vivement recommandé de développer dans un environnement de type Unix.

Pour mysql &gt;= 5.7, il y a une étape supplémentaire:

```
mysql -u**** -p
set global sql_mode='';
exit;
```

### Installation

#### 1. Depuis une archive pré-construite

Un fichier compressé contenant tout ce qui est nécessaire pour le développement et les tests \(pre-fetched sources, database dump, etc.\) est disponible à chaque release de la platforme à packages.claroline.net/releases. C'est le moyen le plus rapide pour démarrer:

```
curl packages.claroline.net/releases/latest/claroline-17.01.tar.gz | tar xzv
cd claroline-17.01
php scripts/configure.php
composer fast-install
```

#### 2. Depuis la source

La procédure d'installation brute comprend plusieurs étapes à suivre dans l'ordre \(extraction des sources php, installation des dépendances dev, construction, création de la base de données, etc.\). À l'exception de l'étape de configuration, la procédure entière se fait au moyen de scripts composer listés dans le fichier composer.json. Pour une installation à partir de zéro, les commandes sont:

```
git clone http://github.com/claroline/Claroline
cd Claroline
php scripts/configure.php
composer sync-dev
```

#### 3. Depuis le web

```
curl packages.claroline.net/releases/latest/claroline-16.05.tar.gz | tar xzv
```

Ouvrez /install.php depuis votre serveur web et suivez les instructions.

### Mise à jour

Pour mettre à jour une installation de développement existante, faites un "pull" des changements les plus récents \(ou d'une version spécifique\) de ce dépôt et utilisez le script sync-dev:

```
git pull
composer sync-dev
```

### Développement

Quelques assets de la plateforme sont gérés par webpack. Dans un environnement de développement, il faut que le webpack dev server soit lancé. Vous pouvez le démarrer avec la commande:

```
npm run watch
```

De toute évidence, vous aurez aussi besoin d'un serveur web intégrant php pour lancer l'application. Une alternative est disponible:

#### 1. En utilisant le serveur web intégré dans PHP

Ceci est la manière la plus simple et la plus conseillée pour lancer l'application en mode développement. Pour démarrer le serveur, utilisez la commande fournie par le framework symfony \(plus de détails ici\):

```
php app/console server:start
```

L'application sera accessible à l'adresse [http://localhost:8000](http://localhost:8000).

#### 2. En utilisant un serveur web indépendant

Si vous désirez utiliser Apache ou Nginx pour votre développement, assurez-vous qu'ils utilisent votre répertoire web et qu'ils accèdent à l'application à l'adresse [http://localhost/example-site/app\_dev.php](http://localhost/example-site/app_dev.php).

Vous devrez certainement régler des droits sur les répertoires suivants:

```
app/config
app/logs
app/sessions
files
web/uploads
```

Vous devez avoir les droits d'écriture sur chaque répertoire tant côté serveur que côté client. Pour plus d'informations sur le sujet, reportez-vous au chapitre sur la configuration dans la documentation officielle de Symfony.

### Utilisation

Vous pouvez créer un premier utilisateur admin avec la commande:

```
php app/console claroline:user:create -a
```

### Plugins

Les plugins sont gérés par composer tout comme tous les autres paquets de la plateforme. Pour installer ou désinstaller les sources d'un plugin, vous l'ajoutez à ou vous l'enlevez de la section concernée du fichier composer.json et vous lancez un update du composer, ou vous utilisez des raccourcis comme composer require,...

Une fois que le paquet du plugin se trouve dans votre répertoire **vendor**, vous pouvez procéder à l'installation ou la d"sinstallation en utilisant les commandes suivantes:

```
php app/console claroline:plugin:install FooBarBundle
php app/console claroline:plugin:uninstall FooBarBundle
```

**Attention:** Les procédures d'installation et de mise à jour de la plateforme telles que décrites plus haut ne s'appliquent qu'à la distribution par défaut qui est livrée avec une paquet déterminé de plugins. Si vous modifiez ce paquet, vous devrez maintenir vos propres fichiers composer files et lancer composer update et php app/console claroline:update en fonction de votre configuration.

### Support navigateurs

Nous vous conseillons d'utiliser Claroline Connect avec les versions les plus récentes de Mozilla Firefox ou Chromium.

Nous supportons:

* Mozilla Firefox \(version la plus récente\)
* Chromium \(version la plus récente\) and Google Chrome \(version la plus récente\)
* Microsoft Edge \(version la plus récente\)
* Microsoft Internet Explorer 11
* Safari \(version la plus récente\)

Pour une liste complète: [http://caniuse.com/\#feat=mutationobserver](http://caniuse.com/#feat=mutationobserver)

### Documentation

Pour la documentation développeurs, voir [https://github.com/claroline/Distribution/blob/master/doc/index.md](https://github.com/claroline/Distribution/blob/master/doc/index.md).

