Vérifier la version de docker compose :
```bash
docker compose version
```


Spécifier la version du docker compose.
```Docker compose
version: 'insérer version'
```

A la suite de ceci, afin de faire tout ce bloc : 

```MD
Contient un service jigglypuff-server qui: 
– construit son image en utilisant le Dockerfile de l'étape précédente ;
– publie le port 3000 du conteneur vers le port 8080 de l'hôte ;
– rend Jigglypuff ”shiny” en définissant la variable d'environnement JIGGLYPUFF à shiny, via une variable d'environnement ou un fichier d'environnement
```

Explications lignes par lignes:
Appelle le service :
```Dockerfile
services:
	jigglypuff-server:
```

Après une tabulation, définir l'image avec le dockerfile :
```Dockerfile
build:
	.
```

Définir les différents ports : 
```Dockerfile
	- "NouveauPort:AncienPort"
```

Définir la variable d'environnement  :
```Dockerfile
environment:
	- NOM_DE_LA_VARIABLE=SA_VALEUR
```

Pour la partie nginx :
```Dockerfile
image:
	définir l'image
```

Définir les ports : 
```Dockerfile
ports:
	- "NouveauPort:AncienPort"
```


# ATTENTION

build, ports, environment, image et ports sont alignés, mais les informations après le retour à la ligne après les : sont tabulés une fois, exemple :

```Dockerfile
services:
	jigglypuff-server:
		build:
			Là ou c'est build
```
