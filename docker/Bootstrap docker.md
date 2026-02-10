Pull un image : 
```
docker pull nginx
```

Pull une image dans une version spécifique :
```
docker pull nginx:1.18
```
(remplacer 1.18 par la version souhaitée)

Lancer un conteneur : 
```
docker run nginx:1.18
```
(remplacer 1.18 par la version souhaitée)


Lister les conteneurs en cours d'exécution : 

```
docker ps
```

Arrêter un conteneur : 
```
docker stop <nom ou id du conteneur>
```

Supprimer un conteneur docker : 

```
docker rm <nom ou id du conteneur>
```


Publier sur un port : 

```
docker run -p 8080:80
```
	(Accessible ensuite sur l'adressse web : localhost:8080)


Afficher la date du conteneur :

```
docker exec <nom ou id du conteneur> date
```

Afficher les logs d'un conteneur : 

```
docker logs <nom ou id du conteneur>
```

Afficher les logs en temps réel : 

```
docker logs -f [ou --follow] <nom ou id du conteneur>
```

(Bonus perso)

Afficher les logs avec l'horodatage :

```
docker logs --timestamps <nom ou id du conteneur>
```
