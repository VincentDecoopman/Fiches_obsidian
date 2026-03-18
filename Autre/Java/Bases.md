Méthodes (entendre par là, fonctions) : 
```java
public || private || protected / int || String || void / nomDeLaMéthode(Paramètres){
	corps de la fonction;
}
```

(Si void est mis il ne peux pas y avoir de return)

Attributs (entendre par là, variables) :

```java
public || protected || private / int || String || float / nomDeLAttribut = valeurInitiale (si besoin);
```

(Float = nombre à virgules)

Bonus : si l'Attribut est "static", il sera partagé par toutes les instances (comme le nombre de roues d'une voiture).
Si l'attribut est constant (mot clé "final"), l'attribut ne peux pas être modifié après l'initialisation.

Constructeur :

Il doit avoir le même nom que la classe 
```java
public class Test {
	public Test(Arguments){
		// corps du constructeur
	}
}
```

