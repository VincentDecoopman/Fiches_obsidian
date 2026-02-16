---
tags:
  - Laravel
---
# Prérequis :
Installer PHP et composer, si vous n'avez pas l'un de ces deux outils voici les commandes : 
Mettre à jours les paquets : 
```shell
sudo apt update
```

Installer PHP : 
```shell
sudo apt install php
```

Installer composer : 

```shell
sudo apt install composer
```

Une fois ceci fait, installer Laravel : 

```shell
composer global require laravel/installer
```


Maintenant, créons le projet, dans votre terminal, mettez vous sur le bureau
```shell
cd Bureau/
```

Et tapez : 
```shell
laravel new <nom du projet>
```

Vous pouvez aller plus vite en tapant simplement : 
```shell
cd Bureau/ && laravel new <nom du projet>
```

Si votre terminal vous dis "Laravel est une commande introuvable", redémarrer votre ordinateur (sans déconner ça à fonctionner pour moi).

Après avoir rentrer cette commande, configurer le projet via les différentes options proposer par Laravel selon vos besoins.

Félicitations, vous venez de créer votre premier projet Laravel.

