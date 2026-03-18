# Installation

Pour commencer mettez à jour votre système, puis, installer PHP,  Composer et Laravel

Mettre à jour son système :

```shell
sudo apt update
```


Installer PHP via terminal : 
```shell
sudo apt install php
```

Vous pouvez maintenant installer Laravel (Composer sera installer en même temps) : 

Installer php et les différentes extensions : 
```shell
sudo apt install php php-cli php-common php-mbstring php-xml php-zip php-mysql php-pgsql php-sqlite3 php-json php-bcmath php-gd php-tokenizer php-xmlwriter -y
```

Installer composer :
```shell
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
sudo chmod +x /usr/local/bin/composer   
```

Créer un nouveau projet Laravel : 

```shell
laravel new nom_du_projet
```

*Remplacer nom_du_projet par ce que vous souhaitez*

Une fois ceci fait, choisissez les paramètres souhaités pour votre projet.

