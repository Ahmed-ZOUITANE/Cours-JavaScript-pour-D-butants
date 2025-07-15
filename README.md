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

Souhaites-tu que je te crée un **PDF ou site interactif** basé sur ce cours ? Ou bien veux-tu passer au **niveau avancé (ES6, async/await, fetch API, etc.)** ?
