# 💻 Cours JavaScript pour Débutants

## 📚 Chapitre 1 : Introduction à JavaScript

* **JavaScript** est un langage de programmation utilisé principalement pour rendre les pages web interactives.
* Il fonctionne côté **client** (navigateur) mais peut aussi être utilisé côté serveur (ex. avec Node.js).
* Il s'intègre dans le HTML via la balise `<script>` :

```html
<script>
  alert("Bonjour le monde !");
</script>
```

---

## 🔤 Chapitre 2 : Variables et Types de Données

### 🔹 Déclaration de variables :

```js
let nom = "Ahmed";    // Variable modifiable
const age = 23;       // Constante
var ville = "Rabat";  // Ancienne façon (à éviter)
```

### 🔹 Types de données :

* Chaîne de caractères : `"texte"`
* Nombre : `42`, `3.14`
* Booléen : `true`, `false`
* Objet : `{ nom: "Ali", age: 30 }`
* Tableau : `[1, 2, 3]`
* Null / Undefined

---

## 🔁 Chapitre 3 : Opérations & Conditions

### 🔹 Opérations :

```js
let a = 5 + 3;      // Addition
let b = 10 - 4;     // Soustraction
let c = 2 * 6;      // Multiplication
let d = 10 / 2;     // Division
let reste = 7 % 2;  // Modulo
```

### 🔹 Conditions :

```js
if (age >= 18) {
  console.log("Majeur");
} else {
  console.log("Mineur");
}
```

---

## 🔁 Chapitre 4 : Boucles

### 🔹 Boucle for :

```js
for (let i = 0; i < 5; i++) {
  console.log("i = " + i);
}
```

### 🔹 Boucle while :

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

## 🧰 Chapitre 5 : Fonctions

```js
function saluer(nom) {
  console.log("Bonjour " + nom);
}

saluer("Ahmed");
```

---

## 📦 Chapitre 6 : Tableaux & Objets

### 🔹 Tableaux :

```js
let fruits = ["pomme", "banane", "orange"];
console.log(fruits[1]); // banane
```

### 🔹 Objets :

```js
let personne = {
  nom: "Sara",
  age: 25,
  saluer: function() {
    console.log("Salut !");
  }
};

personne.saluer();
```

---

## 📋 Chapitre 7 : Manipulation du DOM (Document Object Model)

```html
<p id="texte">Bonjour</p>
<button onclick="changerTexte()">Changer</button>

<script>
function changerTexte() {
  document.getElementById("texte").innerHTML = "Salut le monde";
}
</script>
```

---

## 🌐 Chapitre 8 : Événements

```js
document.getElementById("monBouton").addEventListener("click", function() {
  alert("Bouton cliqué !");
});
```

---

## 🚀 Chapitre 9 : Projet Mini Calculatrice (exemple)

```html
<input type="number" id="a">
<input type="number" id="b">
<button onclick="addition()">Addition</button>
<p id="resultat"></p>

<script>
function addition() {
  let a = Number(document.getElementById("a").value);
  let b = Number(document.getElementById("b").value);
  document.getElementById("resultat").innerText = a + b;
}
</script>
```

---

# 🧱 Cours POO en JavaScript

La **programmation orientée objet (POO)** est un paradigme basé sur l’usage d’**objets** qui contiennent à la fois des **données** (attributs) et des **comportements** (méthodes).

---

## 🔹 1. Déclaration d’une classe

```js
class Personne {
  constructor(nom, age) {
    this.nom = nom;
    this.age = age;
  }

  saluer() {
    console.log(`Bonjour, je m'appelle ${this.nom} et j'ai ${this.age} ans.`);
  }
}
```

---

## 🔹 2. Instanciation d’un objet

```js
let personne1 = new Personne("Ahmed", 25);
personne1.saluer(); // Bonjour, je m'appelle Ahmed et j'ai 25 ans.
```

---

## 🔹 3. Propriétés et méthodes

* **this.nom** → propriété
* **saluer()** → méthode

---

## 🔹 4. Héritage (extends)

```js
class Etudiant extends Personne {
  constructor(nom, age, filiere) {
    super(nom, age); // Appel du constructeur de la classe mère
    this.filiere = filiere;
  }

  info() {
    console.log(`${this.nom} étudie en ${this.filiere}.`);
  }
}

let etu = new Etudiant("Sara", 22, "Informatique");
etu.saluer(); // Hérité de Personne
etu.info();   // Propre à Etudiant
```

---

## 🔹 5. Encapsulation (public/private)

Avec JS moderne (depuis ES2022), on peut définir des **champs privés** avec `#`.

```js
class CompteBancaire {
  #solde = 0;

  deposer(montant) {
    if (montant > 0) {
      this.#solde += montant;
    }
  }

  afficherSolde() {
    console.log(`Solde: ${this.#solde} MAD`);
  }
}

let compte = new CompteBancaire();
compte.deposer(500);
compte.afficherSolde(); // Solde: 500 MAD
// compte.#solde = 1000; ❌ Erreur : accès interdit
```

---

## 🔹 6. Polymorphisme

Le **polymorphisme** permet à une méthode d’avoir un comportement différent selon l’objet.

```js
class Animal {
  parler() {
    console.log("L'animal fait un bruit.");
  }
}

class Chien extends Animal {
  parler() {
    console.log("Le chien aboie.");
  }
}

class Chat extends Animal {
  parler() {
    console.log("Le chat miaule.");
  }
}

let animaux = [new Chien(), new Chat()];
animaux.forEach(animal => animal.parler());
```

---

## 🔹 7. Exemple complet

```js
class Vehicule {
  constructor(marque) {
    this.marque = marque;
  }

  demarrer() {
    console.log(`${this.marque} démarre`);
  }
}

class Voiture extends Vehicule {
  constructor(marque, modele) {
    super(marque);
    this.modele = modele;
  }

  demarrer() {
    console.log(`${this.marque} ${this.modele} démarre en trombe 🚗💨`);
  }
}

let v1 = new Voiture("Toyota", "Corolla");
v1.demarrer();
```

---

## ✅ Résumé des Concepts POO en JS

| Concept        | Mot-clé JS   | Exemple rapide                    |
| -------------- | ------------ | --------------------------------- |
| Classe         | `class`      | `class Personne {}`               |
| Objet          | `new`        | `new Personne()`                  |
| Héritage       | `extends`    | `class Etudiant extends Personne` |
| Appel mère     | `super()`    | `super(nom, age)`                 |
| Attribut privé | `#`          | `#solde`                          |
| Méthode        | `fonction()` | `saluer()`                        |



