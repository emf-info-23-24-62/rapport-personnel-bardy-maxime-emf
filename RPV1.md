# 🤔 RP - 323 - Programmation fonctionnelle

>[!TIP]
>**Référence Javascript:** <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference>  
>**Tester du code JS** : <https://runjs.app/play>  
>**Convertir en PDF** : <https://marketplace.visualstudio.com/items?itemName=manuth.markdown-converter>

# Table des matières

- [🤔 RP - 323 - Programmation fonctionnelle](#-rp---323---programmation-fonctionnelle)
- [Table des matières](#table-des-matières)
- [Introduction](#introduction)
- [Opérateurs javascript super-cooool 😎](#opérateurs-javascript-super-cooool-)
  - [opérateur `?:`](#opérateur-)
  - [opérateur `??`](#opérateur--1)
  - [opérateur `??=`](#opérateur--2)
  - [opérateur de décomposition 'spread' `...`](#opérateur-de-décomposition-spread-)
  - [Déstructuration](#déstructuration)
- [Date et Heure](#date-et-heure)
  - [Obtenir la date et/ou heure actuelle](#obtenir-la-date-etou-heure-actuelle)
- [Math](#math)
  - [`Math.PI` - la constante π](#mathpi---la-constante-π)
  - [`Math.abs()` - la |valeur absolue| d'un nombre](#mathabs---la-valeur-absolue-dun-nombre)
  - [`Math.pow()` - élever à une puissance](#mathpow---élever-à-une-puissance)
  - [`Math.min()` - plus petite valeur](#mathmin---plus-petite-valeur)
  - [`Math.max()` - plus grande valeur](#mathmax---plus-grande-valeur)
  - [`Math.ceil()` - arrondir à la prochaine valeur entière la plus proche](#mathceil---arrondir-à-la-prochaine-valeur-entière-la-plus-proche)
  - [`Math.floor()` - arrondir à la précédente valeur entière la plus proche](#mathfloor---arrondir-à-la-précédente-valeur-entière-la-plus-proche)
  - [`Math.round()` - arrondir à la valeur entière la plus proche](#mathround---arrondir-à-la-valeur-entière-la-plus-proche)
  - [`Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre](#mathtrunc---supprime-la-virgule-et-retourne-la-partie-entière-dun-nombre)
  - [`Math.sqrt()` - la raçine carrée d'un nombre](#mathsqrt---la-raçine-carrée-dun-nombre)
  - [`Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)](#mathrandom---générer-un-nombre-aléatoire-entre-00-compris-et-10-non-compris)
- [JSON](#json)
  - [`JSON.stringify()` - transformer un objet Javascript en JSON](#jsonstringify---transformer-un-objet-javascript-en-json)
  - [`JSON.parse()` - transformer du JSON en objet Javascript](#jsonparse---transformer-du-json-en-objet-javascript)
- [Chaînes de caractères](#chaînes-de-caractères)
  - [`split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau](#split---un-ciseau-qui-coupe-une-chaîne-là-où-un-caractère-apparaît-et-produit-un-tableau)
  - [`trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)](#trim-trimstart-et-trimend---épuration-des-espaces-en-trop-dans-une-chaîne-trimming)
  - [`padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères](#padstart-et-padend---aligner-le-contenu-dans-une-chaîne-de-caractères)
- [Console](#console)
  - [`console.log()` - Afficher un message sur la console](#consolelog---afficher-un-message-sur-la-console)
  - [`console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)](#consoleinfo-warn-et-error---afficher-un-message-sur-la-console-filtrables)
  - [`console.table()` - Afficher tout un tableau ou un objet sur la console](#consoletable---afficher-tout-un-tableau-ou-un-objet-sur-la-console)
  - [`console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution](#consoletime-timelog-et-timeend---chronométrer-une-durée-dexécution)
- [Tableaux](#tableaux)
  - [`forEach` - parcourir les éléments d'un tableau](#foreach---parcourir-les-éléments-dun-tableau)
  - [`entries()` - parcourir les couples index/valeurs d'un tableau](#entries---parcourir-les-couples-indexvaleurs-dun-tableau)
  - [`in` - parcourir les clés d'un tableau](#in---parcourir-les-clés-dun-tableau)
  - [`of` - parcourir les valeurs d'un tableau](#of---parcourir-les-valeurs-dun-tableau)
  - [`find()` - premier élément qui satisfait une condition](#find---premier-élément-qui-satisfait-une-condition)
  - [`findIndex()` - premier index qui satisfait une condition](#findindex---premier-index-qui-satisfait-une-condition)
  - [`indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond](#indexof-et-lastindexof---premierdernier-élément-qui-correspond)
  - [`push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau](#push-pop-shift-et-unshift---ajoutersupprime-au-débutfin-dans-un-tableau)
  - [`slice()` - ne conserver que certaines lignes d'un tableau](#slice---ne-conserver-que-certaines-lignes-dun-tableau)
  - [`splice()` - supprimer/insérer/remplacer des valeurs dans un tableau](#splice---supprimerinsérerremplacer-des-valeurs-dans-un-tableau)
  - [`concat()` - joindre deux tableaux](#concat---joindre-deux-tableaux)
  - [`join()` - joindre des chaînes de caractères](#join---joindre-des-chaînes-de-caractères)
  - [`keys()` et `values()` - les clés/valeurs d'un objet](#keys-et-values---les-clésvaleurs-dun-objet)
  - [`includes()` - vérifier si une valeur est présente dans un tableau](#includes---vérifier-si-une-valeur-est-présente-dans-un-tableau)
  - [`every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau](#every-et-some---vérifier-si-plusieurs-valeurs-sont-toutesquelques-présentes-dans-un-tableau)
  - [`fill()` - remplir un tableau avec des valeurs](#fill---remplir-un-tableau-avec-des-valeurs)
  - [`flat()` - aplatir un tableau](#flat---aplatir-un-tableau)
  - [`sort()` - pour trier un tableau](#sort---pour-trier-un-tableau)
  - [`map()` - tableau avec les résultats d'une fonction](#map---tableau-avec-les-résultats-dune-fonction)
  - [`filter()` - tableau avec les éléments passant un test](#filter---tableau-avec-les-éléments-passant-un-test)
  - [`groupBy()` - regroupe les éléments d'un tableau selon un règle](#groupby---regroupe-les-éléments-dun-tableau-selon-un-règle)
  - [`flatMap()` - chaînage de map() et flat()](#flatmap---chaînage-de-map-et-flat)
  - [`reduce()` et `reduceRight()` - réduire un tableau à une seule valeur](#reduce-et-reduceright---réduire-un-tableau-à-une-seule-valeur)
  - [`reverse()` - inverser l'ordre du tableau](#reverse---inverser-lordre-du-tableau)
- [Techniques](#techniques)
  - [(backticks) - pour des expressions intelligentes](#backticks---pour-des-expressions-intelligentes)
  - [`new Set()` - pour supprimer les doublons](#new-set---pour-supprimer-les-doublons)
- [Fonctions](#fonctions)
  - [Déclaration de fonction](#déclaration-de-fonction)
  - [Fonctions immédiatement invoquées (IIFE)](#fonctions-immédiatement-invoquées-iife)
- [Conclusion](#conclusion)

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Introduction

> Votre introduction avec notamment les objectifs opérationnels du module.

# Opérateurs javascript super-cooool 😎

## opérateur `?:`

> L'expression `question?valeur1:valeur2` retournera `valeur1` si `question` vaut `true` sinon elle retournera `valeur2`.

```javascript
const age = 15;
const resultat = age >= 18 ? 'majeur' : 'mineur'; // 'mineur'
```

## opérateur `??`

Cet opérateur logique se nomme l'opérateur de "coalescence des nuls".

> Renvoie son opérande de droite lorsque son opérande de gauche vaut `null` ou `undefined` et qui renvoie son opérande de gauche sinon.

```javascript
const foo1 = null ?? 'default'; // "default"
const foo2 = 0 ?? 42; // 0
```

>[!CAUTION]
>Contrairement à l'opérateur logique OU (`||`), l'opérande de gauche sera également renvoyé s'il s'agit d'une valeur équivalente à `false` et pas seulement `null` et `undefined`.
>
>⚠️ En d'autres termes **ATTENTION** ‼️ lors de l'utilisation de `||` pour fournir une valeur par défaut à une variable, car on peut rencontrer des comportements inattendus lorsqu'on considère certaines valeurs comme correctes et utilisables (par exemple une chaine vide `''` ou `0`) ‼️

```javascript
const foo3 = 0 || 42; // 42 => ATTENTION !
const foo4 = 1 || 42; // 1
const foo5 = null || 'salut !'; // 'salut !'
const foo6 = '' || 'salut !'; // 'salut !' => ATTENTION !
```

## opérateur `??=`

Cet opérateur logique se nomme l'opérateur d'affectation de "coalescence des nuls", également connu sous le nom d'opérateur affectation logique nulle.

> Évalue l'opérande de droite et l'attribue à gauche **UNIQUEMENT si l'opérande de gauche est nulle** (`null` ou `undefined`).

```javascript
const a = { duration: 50 };
a.duration ??= 10; // pas fait
a.speed ??= 25; // fait => { duration: 50, speed: 25 }
```

## opérateur de décomposition 'spread' `...`

L'opérateur de décomposition spread `...` permet de décomposer un itérable (comme un tableau) en en ses éléments distincts. Cela permet de rapidement copier tout ou une partie d'un tableau existant dans un autre tableau ou d'en extraire facilement des parties.

```javascript
// Combiner des valeurs existantes dans un nouveau tableau
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

// Extraire uniquement ce qui est utile d'un tableau
const numbers = [1, 2, 3, 4, 5, 6];
const [one, two, ...rest] = numbers;

// Mariage d'objets avec mise à jour :-)
const myVehicle = {
    brand: 'Ford',
    model: 'Mustang',
    color: 'red',
};
const updateMyVehicle = {
    type: 'car',
    year: 2021,
    color: 'yellow',
};
const myUpdatedVehicle = { ...myVehicle, ...updateMyVehicle };
```

## Déstructuration

L'opérateur de décomposition spread `...` sert aussi à isoler certains éléments afin de les utiliser ensuite, et de **mettre le reste** d'un coup ailleurs.

```javascript
const valeurs = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const [a, b, ...c] = valeurs;
console.log(a); // 1
console.log(b); // 2
console.log(c); // [3, 4, 5, 6, 7, 8, 9, 10]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Date et Heure

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date)

## Obtenir la date et/ou heure actuelle

```javascript
const maintenant = new Date(); // Obtenir l'un comme l'autre

console.log(maintenant.toLocaleDateString()); // ex: "06.06.2025"
console.log(maintenant.toLocaleTimeString()); // ex: "15:23:42"

const jour = maintenant.getDate();
const mois = maintenant.getMonth() + 1; // Attention : janvier = 0
const annee = maintenant.getFullYear();
const heure = maintenant.getHours();
const minute = maintenant.getMinutes();
const seconde = maintenant.getSeconds();
console.log(`${jour}/${mois}/${annee} - ${heure}h${minute}`);

// Au format ISO (standard international)
console.log(maintenant.toISOString()); // ex: "2025-06-06T13:23:42.123Z"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Math

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math)

## `Math.PI` - la constante π

La propriété `Math.PI` fournit la valeur de la constante mathématique π (pi), c'est‑à‑dire le rapport entre la circonférence d’un cercle et son diamètre. Elle est souvent utilisée pour calculer des périmètres ou des aires de cercles.

```javascript
console.log(Math.PI); // 3.141592653589793
const rayon = 5;
const perimetre = 2 * Math.PI * rayon;
console.log(perimetre); // 31.41592653589793
```

## `Math.abs()` - la |valeur absolue| d'un nombre

`Math.abs()` renvoie la valeur absolue d’un nombre, c’est‑à‑dire sa distance à zéro. Les nombres négatifs deviennent positifs, les nombres positifs sont retournés tels quels.

```javascript
console.log(Math.abs(-42)); // 42
console.log(Math.abs(3.14)); // 3.14
```

## `Math.pow()` - élever à une puissance

`Math.pow(base, exposant)` élève un nombre à une puissance donnée. C’est l’équivalent fonctionnel de l’opérateur d’exponentiation `**`.

```javascript
console.log(Math.pow(2, 3)); // 8
// opérateur équivalent
console.log(2 ** 3); // 8
```

## `Math.min()` - plus petite valeur

`Math.min()` renvoie la plus petite valeur parmi une liste de nombres. On peut l’utiliser avec l’opérateur spread pour déterminer le minimum d’un tableau.

```javascript
console.log(Math.min(4, 2, 8)); // 2
const arr = [5, 3, 9];
console.log(Math.min(...arr)); // 3
```

## `Math.max()` - plus grande valeur

`Math.max()` renvoie la plus grande valeur parmi une liste de nombres. Comme pour `Math.min()`, l’opérateur spread permet de l’appliquer à un tableau.

```javascript
console.log(Math.max(4, 2, 8)); // 8
const arr = [5, 3, 9];
console.log(Math.max(...arr)); // 9
```

## `Math.ceil()` - arrondir à la prochaine valeur entière la plus proche

`Math.ceil()` arrondit un nombre à l’entier supérieur le plus proche. Si le nombre est déjà un entier, il est renvoyé tel quel.

```javascript
console.log(Math.ceil(4.2)); // 5
console.log(Math.ceil(-1.1)); // -1
```

## `Math.floor()` - arrondir à la précédente valeur entière la plus proche

`Math.floor()` arrondit un nombre à l’entier inférieur le plus proche. Utile pour tronquer les décimales lorsque l’on souhaite partir vers le bas.

```javascript
console.log(Math.floor(4.9)); // 4
console.log(Math.floor(-1.1)); // -2
```

## `Math.round()` - arrondir à la valeur entière la plus proche

`Math.round()` arrondit un nombre à l’entier le plus proche. Les valeurs en .5 sont arrondies vers le haut.

```javascript
console.log(Math.round(4.5)); // 5
console.log(Math.round(4.4)); // 4
```

## `Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre

`Math.trunc()` supprime la partie décimale d’un nombre et renvoie uniquement la partie entière, sans arrondi. Le signe du nombre est conservé.

```javascript
console.log(Math.trunc(4.9)); // 4
console.log(Math.trunc(-1.7)); // -1
```

## `Math.sqrt()` - la raçine carrée d'un nombre

`Math.sqrt()` renvoie la racine carrée d’un nombre positif. Pour un nombre négatif, le résultat est `NaN` (Not‑a‑Number).

```javascript
console.log(Math.sqrt(9)); // 3
console.log(Math.sqrt(2)); // 1.4142135623730951
```

## `Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)

`Math.random()` produit un nombre pseudo‑aléatoire compris entre 0 inclus et 1 exclus. On peut ensuite l’adapter à un intervalle souhaité, par exemple pour tirer un entier dans une plage.

```javascript
const r = Math.random(); // 0 <= r < 1
// nombre entier entre 1 et 6 inclus (simulation d’un dé)
const dice = Math.floor(Math.random() * 6) + 1;
console.log(dice);
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# JSON

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON)

## `JSON.stringify()` - transformer un objet Javascript en JSON

`JSON.stringify(objet)` convertit un objet ou un tableau JavaScript en une chaîne JSON. On peut fournir un replacer (pour filtrer ou transformer les valeurs) et un argument `space` pour formater la sortie de manière lisible.

```javascript
const obj = { name: 'Alice', age: 25 };
const jsonString = JSON.stringify(obj); // '{"name":"Alice","age":25}'
// Formattage sur plusieurs lignes pour débogage
const pretty = JSON.stringify(obj, null, 2);
console.log(pretty);
```

## `JSON.parse()` - transformer du JSON en objet Javascript

`JSON.parse(chaine)` analyse une chaîne JSON et renvoie l’objet ou le tableau correspondant. Un deuxième argument optionnel permet de transformer les valeurs via un "reviver".

```javascript
const text = '{"name":"Alice","age":25}';
const user = JSON.parse(text);
console.log(user.name); // 'Alice'
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Chaînes de caractères

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String)

## `split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau

La méthode `split(séparateur, limite?)` découpe une chaîne en plusieurs sous‑chaînes à chaque occurrence du séparateur et renvoie un tableau des morceaux. La chaîne d’origine n’est pas modifiée. Si le séparateur est une chaîne vide, la chaîne est scindée caractère par caractère.

```javascript
const phrase = 'chien;chat;lapin';
const animaux = phrase.split(';'); // ['chien', 'chat', 'lapin']
const lettres = 'bonjour'.split(''); // ['b','o','n','j','o','u','r']
```

## `trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)

Ces méthodes retirent les espaces blancs (et les retours à la ligne) en début et/ou fin de chaîne. `trim()` supprime des deux côtés, `trimStart()` (ou `trimLeft()`) uniquement au début et `trimEnd()` (ou `trimRight()`) uniquement à la fin. La chaîne retournée est une nouvelle chaîne.

```javascript
const brut = '   hello world   ';
console.log(brut.trim()); // 'hello world'
console.log(brut.trimStart()); // 'hello world   '
console.log(brut.trimEnd()); // '   hello world'
```

## `padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères

`padStart(longueur, remplissage)` et `padEnd(longueur, remplissage)` complètent une chaîne avec des caractères afin qu’elle atteigne une longueur donnée. Par défaut, les espaces sont utilisés comme remplissage. C’est pratique pour afficher des nombres alignés.

```javascript
const code = '5';
console.log(code.padStart(3, '0')); // '005'
console.log(code.padEnd(3, '.')); // '5..'
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Console

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/API/console](https://developer.mozilla.org/fr/docs/Web/API/console)

## `console.log()` - Afficher un message sur la console

```javascript
console.log('Coucou !'); // Coucou !
```

## `console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)

Ces méthodes permettent de journaliser des messages avec différents niveaux de sévérité. Dans les outils de développement du navigateur, elles peuvent être filtrées ou apparaître avec une icône distincte.

```javascript
console.info('Démarrage'); // message d’information
console.warn('Attention : valeur élevée'); // message d’avertissement
console.error('Oups, quelque chose ne va pas'); // message d’erreur
```

## `console.table()` - Afficher tout un tableau ou un objet sur la console

`console.table()` affiche les éléments d’un tableau ou les propriétés d’un objet sous forme de tableau. Chaque élément devient une ligne, et les propriétés deviennent des colonnes, ce qui facilite la lecture des données en console.

```javascript
const personnes = [
  { nom: 'Alice', age: 25 },
  { nom: 'Bob', age: 30 }
];
console.table(personnes);
```

## `console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution

Ces méthodes aident à mesurer le temps d’exécution d’un bout de code. `console.time(label)` démarre un chronomètre identifié par `label`, `console.timeLog(label)` affiche le temps écoulé sans l’arrêter et `console.timeEnd(label)` affiche le temps total et arrête le chronomètre.

```javascript
console.time('boucle');
for (let i = 0; i < 1e6; i++) {}
console.timeLog('boucle'); // ~x ms depuis le début
console.timeEnd('boucle'); // ~x ms au total
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Tableaux

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array)

## `forEach` - parcourir les éléments d'un tableau

`forEach(callback[, thisArg])` exécute une fonction pour chaque élément du tableau. Il est utilisé pour parcourir un tableau lorsqu’on souhaite produire des effets de bord (log, modification d’objets…) mais il ne renvoie pas de nouvelle liste.

```javascript
const nombres = [1, 2, 3];
nombres.forEach((n) => {
  console.log(n * 2);
});
```

## `entries()` - parcourir les couples index/valeurs d'un tableau

La méthode `entries()` renvoie un itérateur qui fournit des paires `[index, valeur]` pour chaque élément du tableau. Cela permet de parcourir simultanément l’index et la valeur via un `for...of`.

```javascript
const letters = ['a', 'b', 'c'];
for (const [index, value] of letters.entries()) {
  console.log(index, value);
}
// 0 'a', 1 'b', 2 'c'
```

## `in` - parcourir les clés d'un tableau

L’instruction `for...in` parcourt les clés énumérables d’un objet. Utilisée sur un tableau, elle itère sur les indices (sous forme de chaînes) et sur les propriétés héritées. Elle est donc rarement utilisée pour les tableaux, mais elle reste utile pour énumérer les propriétés d’un objet.

```javascript
const arr = [10, 20, 30];
for (const index in arr) {
  console.log(index, arr[index]);
}
// 0 10, 1 20, 2 30
```

## `of` - parcourir les valeurs d'un tableau

`for...of` permet d’itérer directement sur les valeurs d’un itérable (tableau, chaîne de caractères, Set, Map…). Contrairement à `for...in`, il ignore les propriétés non numériques et héritées.

```javascript
for (const value of [10, 20, 30]) {
  console.log(value);
}
// 10, 20, 30
```

## `find()` - premier élément qui satisfait une condition

`find(predicate[, thisArg])` renvoie le premier élément du tableau qui vérifie la condition donnée. Si aucun élément ne correspond, la valeur `undefined` est renvoyée.

```javascript
const nombres = [1, 5, 10];
const grand = nombres.find((n) => n > 4); // 5
const manquant = nombres.find((n) => n < 0); // undefined
```

## `findIndex()` - premier index qui satisfait une condition

`findIndex(predicate[, thisArg])` renvoie l’indice du premier élément qui vérifie la condition. Si aucun élément ne correspond, la méthode renvoie `-1`.

```javascript
const nombres = [1, 5, 10];
const i = nombres.findIndex((n) => n > 4); // 1
const j = nombres.findIndex((n) => n < 0); // -1
```

## `indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond

`indexOf(valeur, début?)` recherche la première occurrence d’une valeur simple (chaine, nombre…) dans le tableau et renvoie son indice ou `-1` si elle est absente. `lastIndexOf()` fait la même chose depuis la fin du tableau.

```javascript
const fruits = ['pomme', 'banane', 'pomme'];
console.log(fruits.indexOf('pomme')); // 0
console.log(fruits.lastIndexOf('pomme')); // 2
```

## `push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau

Ces quatre méthodes modifient directement le tableau. `push(...éléments)` ajoute un ou plusieurs éléments à la fin et retourne la nouvelle longueur. `pop()` supprime et renvoie le dernier élément. `unshift(...éléments)` ajoute au début et renvoie la nouvelle longueur. `shift()` retire et renvoie le premier élément.

```javascript
const stack = [1, 2];
stack.push(3); // [1,2,3]
const last = stack.pop(); // 3, stack devient [1,2]
const queue = [1,2];
queue.unshift(0); // [0,1,2]
const first = queue.shift(); // 0, queue devient [1,2]
```

## `slice()` - ne conserver que certaines lignes d'un tableau

`slice(début, fin?)` crée une copie superficielle d’une portion du tableau comprise entre `début` (inclus) et `fin` (exclu). Les indices négatifs comptent depuis la fin. Le tableau d’origine n’est pas modifié.

```javascript
const arr = [0,1,2,3,4];
console.log(arr.slice(1,3)); // [1,2]
console.log(arr.slice(-2)); // [3,4]
```

## `splice()` - supprimer/insérer/remplacer des valeurs dans un tableau

`splice(début, nombreASupprimer, ...éléments)` modifie le tableau à l’endroit donné : elle supprime `nombreASupprimer` éléments à partir de l’indice `début` et insère éventuellement de nouveaux éléments à la même position. Elle renvoie un tableau contenant les éléments supprimés.

```javascript
const arr = [1, 2, 3, 4];
arr.splice(1, 2, 'a', 'b'); // supprime 2, insère 'a','b'
console.log(arr); // [1,'a','b',4]
arr.splice(2, 0, 99); // insère 99 à l'index 2
console.log(arr); // [1,'a',99,'b',4]
```

## `concat()` - joindre deux tableaux

`concat(...listes)` renvoie un nouveau tableau résultant de la concaténation des listes fournies. Le tableau d’origine et les arguments ne sont pas modifiés.

```javascript
const a = [1, 2];
const b = [3, 4];
const c = a.concat(b); // [1,2,3,4]
console.log(a); // [1,2], inchangé
```

## `join()` - joindre des chaînes de caractères

`join(séparateur?)` concatène les éléments d’un tableau en une chaîne, en utilisant `séparateur` pour séparer les éléments. Sans argument, une virgule est utilisée.

```javascript
const mots = ['Hello','world'];
console.log(mots.join(' ')); // 'Hello world'
console.log([1,2,3].join('-')); // '1-2-3'
```

## `keys()` et `values()` - les clés/valeurs d'un objet

Pour manipuler les propriétés d’un objet, JavaScript propose plusieurs méthodes. `Object.keys(obj)` renvoie un tableau contenant les noms de propriétés propres de l’objet. `Object.values(obj)` renvoie un tableau de leurs valeurs. `Object.entries(obj)` renvoie un tableau de couples `[clé, valeur]`, et `Object.fromEntries()` effectue l’opération inverse en créant un objet à partir d’une liste de paires. Ces outils sont très pratiques pour transformer un objet en tableau et inversement ou pour itérer sur ses propriétés.

```javascript
const obj = { a: 1, b: 2 };
const keys = Object.keys(obj); // ['a','b']
const values = Object.values(obj); // [1,2]
const entries = Object.entries(obj); // [['a',1], ['b',2]]
const obj2 = Object.fromEntries(entries); // { a:1, b:2 }
```

## `includes()` - vérifier si une valeur est présente dans un tableau

`includes(valeur, départ?)` renvoie `true` si le tableau contient la valeur spécifiée, `false` sinon. La recherche utilise l’égalité stricte (`===`) et peut démarrer à l’indice `départ`.

```javascript
const arr = [1,2,3];
console.log(arr.includes(2)); // true
console.log(arr.includes(4)); // false
console.log(arr.includes(1, 1)); // false (on commence la recherche à l'indice 1)
```

## `every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau

`every(predicate)` retourne `true` si **tous** les éléments satisfont la condition, ou si le tableau est vide. `some(predicate)` retourne `true` si **au moins un** élément satisfait la condition.

```javascript
const nums = [2,4,6];
console.log(nums.every(n => n % 2 === 0)); // true
console.log(nums.some(n => n > 5)); // true
```

## `fill()` - remplir un tableau avec des valeurs

`fill(valeur, début?, fin?)` remplit tout ou partie du tableau avec une valeur statique. La méthode modifie le tableau sur lequel elle est appelée.

```javascript
const arr = [1,2,3,4];
arr.fill(0, 1, 3); // [1,0,0,4]
const zeros = new Array(3).fill(0); // [0,0,0]
```

## `flat()` - aplatir un tableau

`flat(profondeur?)` retourne un nouveau tableau avec les éléments de sous‑tableaux concaténés jusqu’à la profondeur spécifiée. Par défaut, `flat()` ne fait qu’un niveau d’aplatissement.

```javascript
const arr = [1, [2, [3]]];
console.log(arr.flat()); // [1,2,[3]]
console.log(arr.flat(2)); // [1,2,3]
```

## `sort()` - pour trier un tableau

`sort(compareFn?)` trie les éléments d’un tableau **sur place** et renvoie le tableau trié. Par défaut, les éléments sont convertis en chaînes et triés selon l’ordre Unicode. Pour trier des nombres ou selon un critère personnalisé, on passe une fonction de comparaison.

```javascript
const names = ['Bob','Alice','Eve'];
names.sort(); // ['Alice','Bob','Eve']
const nums = [3,10,1];
nums.sort((a,b) => a - b); // [1,3,10]
```

## `map()` - tableau avec les résultats d'une fonction

`map(callback[, thisArg])` applique une fonction à chaque élément et renvoie un **nouveau** tableau contenant les résultats. L’original n’est pas modifié.

```javascript
const nums = [1,2,3];
const squares = nums.map(n => n * n); // [1,4,9]
console.log(nums); // [1,2,3]
```

## `filter()` - tableau avec les éléments passant un test

`filter(predicate[, thisArg])` sélectionne les éléments qui passent le test défini dans la fonction et renvoie un nouveau tableau. Si aucun élément ne correspond, on obtient un tableau vide.

```javascript
const nums = [1,2,3,4];
const even = nums.filter(n => n % 2 === 0); // [2,4]
```

## `groupBy()` - regroupe les éléments d'un tableau selon un règle

La méthode `groupBy()` (exposée par `Object.groupBy()` ou par `Array.prototype.groupBy()` selon les versions) permet de regrouper les éléments d’une collection en fonction de la valeur renvoyée par un callback. Le résultat est un objet dont chaque propriété correspond à une clé de groupe et contient un tableau des éléments associés. Cette fonctionnalité est disponible dans les navigateurs récents.

```javascript
const users = [
  {name:'Alice', role:'admin'},
  {name:'Bob', role:'user'},
  {name:'Carol', role:'admin'}
];
const parRole = Object.groupBy(users, u => u.role);
console.log(parRole.admin);
// [ {name:'Alice', role:'admin'}, {name:'Carol', role:'admin'} ]
```

## `flatMap()` - chaînage de map() et flat()

`flatMap(callback[, thisArg])` combine le comportement de `map()` suivi de `flat(1)`. Il applique la fonction de transformation à chaque élément et aplatit ensuite d’un niveau le résultat. C’est très utile pour éclater des éléments en plusieurs.

```javascript
const phrases = ['bonjour le monde','salut'];
const mots = phrases.flatMap(p => p.split(' '));
console.log(mots); // ['bonjour','le','monde','salut']
```

## `reduce()` et `reduceRight()` - réduire un tableau à une seule valeur

`reduce(callback, valeurInitiale?)` applique une fonction réductrice à chaque élément, de gauche à droite, pour aboutir à une seule valeur. `reduceRight()` procède dans l’autre sens. Toujours définir `valeurInitiale` pour éviter des comportements inattendus sur des tableaux vides.

```javascript
const nums = [1,2,3,4];
const sum = nums.reduce((acc, val) => acc + val, 0); // 10
const concatReverse = ['a','b','c'].reduceRight((acc, val) => acc + val, ''); // 'cba'
```

## `reverse()` - inverser l'ordre du tableau

`reverse()` renverse l’ordre des éléments **sur place** et renvoie le tableau lui‑même. Utile pour inverser des listes rapidement.

```javascript
const arr = [1,2,3];
arr.reverse(); // [3,2,1]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Techniques

## (backticks) - pour des expressions intelligentes

Les backticks (accent grave) permettent de créer des **templates strings**. Ces chaînes acceptent des expressions dynamiques via la syntaxe `${expression}` et prennent en charge les retours à la ligne sans caractères d’échappement. Elles sont très pratiques pour construire des chaînes multi‑lignes ou injecter des valeurs.

```javascript
const nom = 'Alice';
console.log(`Bonjour ${nom} !`);
const multiLigne = `Ligne 1
Ligne 2`;
console.log(multiLigne);
```

## `new Set()` - pour supprimer les doublons

Un `Set` est une collection d’éléments **uniques**. En l’instanciant avec un tableau, on élimine automatiquement les doublons. On peut ensuite reconvertir le `Set` en tableau en utilisant l’opérateur spread (`...`) ou `Array.from()`.

```javascript
const arr = [1,2,2,3];
const unique = [...new Set(arr)]; // [1,2,3]
const s = new Set();
s.add('a');
s.add('a'); // le doublon est ignoré
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Fonctions

## Déclaration de fonction

**Standard**

```javascript
function doStuff(a, b, c) {
    return a + b + c;
}
```

**Sous forme d'expression de fonction**

```javascript
const doStuff = function (a, b, c) {
    return a + b + c;
};
```

**Sous forme d'expression de fonction anonyme**

```javascript
const doStuff = (a, b, c) => {
    return a + b + c;
};
```

**Sous forme raccourcie**

S'il n'y a qu'un seul argument et que son corps n'a qu'une seule expression, on peut omettre le return et le corps de la fonction :

```javascript
const doStuff = (a) => `Salut ${a} !`;
```

## Fonctions immédiatement invoquées (IIFE)

IIFE = Immediately Invoked Function Expressions.

Ces fonctions sont définies et **exécutées immédiatement**. Elles sont souvent utilisées pour créer un **contexte isolé** ou encapsuler du code sans polluer l’espace global.

```javascript
(function(){ /* code isolé */ })()
```

ou

```javascript
(() => { /* code isolé */ })()
```

# Conclusion

> Votre conclusion avec les éléments usuels
