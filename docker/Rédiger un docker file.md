(Docker file du bootstrap)

Définir image de base
``` dockerfile
FROM <image>
```

Définir le dossier de travail 
```Dockerfile
WORKDIR /dossier
```

Installer quelque chose 
```Dockerfile
RUN <chose à installer>
```

Exposer un port :
```DOCKERFILE
EXPOSE <n° du PORT>
```

Créer la commande :
```DOCKERFILE
CMD ["un mot au choix"]
```

(Si vous souhaitez faire une commande avec plusieurs mots voici comment faire) :
```DOCKERFILE
CMD ["mot1", "mot2" etc etc etc]
```

