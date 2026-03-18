# React : Infos primaires

### 1 - Les composants :

Un composant est une fonction qui retourne du JSX (JavaScript XML)
-> Le JSX est une syntaxe spéciale que React utilise pour écrire du HTML dans du JS.

Exemple simple :

```jsx
function App() {
  return <h1>Hello World !</h1>;
}

export default App;
```

Dans ce code :
"App" est un composant qui retourne du HTML, et React l'affiche sur le navigateur.

### 2 - JSX :

Le JSX ressemble à du HTML, sans l'être exactement.
Tu peux mettre du JS dedans.

Exemple simple :

```jsx
function App() {
  const nom = "John";

  return <h1>Salut {nom}</h1>;
}
```

### 3 - Le State (/!\ assez important) :

Le state est une donnée qui peut changer. Par exemple :

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Compteur : {count}</p>
      <button onClick={() => setCount(count + 1)}>Clique moi !</button>
    </div>
  );
}
```

Quand la valeur change, React l'actualise automatiquement