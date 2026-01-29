http://exemple.com/api/customers

http :
	-Est soit HTTP soit HTTPS (dépend de l'application et des conditions)
	-Si tu veux que les données soient échangées de manières sécurisées : fait le avec HTTPS.

exemple.com : 
	-Nom de domaine de l'application

api : 
	-Beaucoup d'entreprises vont suivre cette convention et vont mettre le mot "API" quelque part dans l'adresse url. (peut être après le domaine ou être un sous domaine)

customers : 
	-Se réfère à la collection des clients (customers en anglais) 
	-On se dit que c'est une ressource 
	-Pour modifier des données dans cette BDD, on envoie des requêtes HTTP
		-Chaque requêtes à un "Verbe"/"Méthode"
			-GET pour obtenir des données
			-POST pour créer des données
			-PUT pour mettre à jour des données
			-DELETE pour supprimer des données

# Exemple de requêtes lié à des clients (customers)
## GET


Requête : 
	-GET /api/customers

Réponse : 
```
[
	{id: 1, name: 'coin coin'},
	{id: 2, name: 'tut tut'},
]
```

Pour avoir un client précis  :

Requête : 
	-GET /api/customers/1

Réponse : 
```
[
	{id: 1, name: 'coin coin'},
]
```

## PUT

Requête : 
	-PUT /api/customers/1 (on spécifie dans cet exemple)
	 {name: 'TIC TAC'};

Réponse : 
	-{id: 1, name: 'TIC TAC'}; (anciennement coin coin).


## DELETE

Requête : 
	-DELETE /api/customers/1 (pas besoin de spécifier l'objet du customer (id, name, adresse etc, quand on supprime, on supprime tout))

Réponse : 
	-Bah ça supprime...j'ai normalement pas besoin d'expliquer :| 

## POST

Requête : 
	-POST /api/customers (pas besoin de spécifier quelque chose après customers vu qu'on s'occupe de la "collection" customers) {name: 'René'}

Réponse : 
	-{id: 1, name: 'René'}

