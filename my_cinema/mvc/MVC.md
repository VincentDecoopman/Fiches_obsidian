"Model View Controller"
Fréquemment utilisé
Sépare les applications fonctionnelles
Favorise la programmation organisée
Design architectural 

# Frameworks utilisant le MVC
- Ruby on rails (ruby)
- Sinatra (ruby)
- Laravel (php)
- COdeigniter (php)
- Zend(PHP)
- Express (JS)
- backbone (JS)
- Angular (JS)
- Django(Python)
- Flask(Python)

# Model :
Relatif à la logique
Intéragi avec les DB (Select, insert, update, delete)
Communique avec le controller,
Peux parfois mettre à jour le view (dépendamment des frameworks)

# View

Ce que l'utilisateur voit
Consiste globalement à du HTML/CSS
Communique avec le controller
Peut recevoir des valeurs dynamiques depuis le controller

# Controller
Recois des inputs (from, view, url)
fais des requettes (Get, post, put, delete)
recois des données de la part du model
Donne des données à la view