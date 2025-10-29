<h1>🤔 RP - 323 - Programmation fonctionnelle</h1>

>[!TIP]
>**Référence Javascript:** <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference>  
>**Tester du code JS** : <https://runjs.app/play>  
>**Convertir en PDF** : <https://marketplace.visualstudio.com/items?itemName=manuth.markdown-converter>

<h1>Table des matières</h1>

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
  - [`for...of` - parcourir les valeurs d'un tableau](#forof---parcourir-les-valeurs-dun-tableau)
  - [`find()` - premier élément qui satisfait une condition](#find---premier-élément-qui-satisfait-une-condition)
  - [`findIndex()` - premier index qui satisfait une condition](#findindex---premier-index-qui-satisfait-une-condition)
  - [`indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond](#indexof-et-lastindexof---premierdernier-élément-qui-correspond)
  - [`push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprimer au début/fin d’un tableau](#push-pop-shift-et-unshift---ajoutersupprimer-au-débutfin-dun-tableau)
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
  - [`groupBy()` - regroupe les éléments d'un tableau selon une règle](#groupby---regroupe-les-éléments-dun-tableau-selon-une-règle)
  - [`flatMap()` - chaînage de map() et flat()](#flatmap---chaînage-de-map-et-flat)
  - [`reduce()` et `reduceRight()` - réduire un tableau à une seule valeur](#reduce-et-reduceright---réduire-un-tableau-à-une-seule-valeur)
  - [`reverse()` - inverser l'ordre du tableau](#reverse---inverser-lordre-du-tableau)
- [Techniques](#techniques)
  - [\`\`(backticks) - pour des expressions intelligentes](#backticks---pour-des-expressions-intelligentes)
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

Constante qui représente π (≈ **3.141592653589793**).
Utile pour **cercles**, **angles** et **trigonométrie**.

```javascript
// périmètre d’un cercle (rayon r)
const r = 5;
const perimetre = 2 * Math.PI * r; // ≈ 31.4159
```

## `Math.abs()` - la \|valeur absolue\| d'un nombre

Renvoie la **valeur absolue** d’un nombre (toujours ≥ 0).
Utile pour **distances**, **écarts**, **valeurs sans signe**. Renvoie `NaN` si l’argument n’est pas convertible en nombre.

```javascript
Math.abs(-7);            // 7
Math.abs(0);             // 0
Math.abs(-3.14);         // 3.14

// Écart (valeur absolue de la différence)
const a = 10, b = 4;
const ecart = Math.abs(a - b); // 6

// Appliquer sur un tableau
[-3, 0, 2].map(Math.abs); // [3, 0, 2]
```

## `Math.pow()` - élever à une puissance

Élève une **base** à une **puissance** : `Math.pow(base, exp)`
Équivalent moderne : `base ** exp`.

```javascript
Math.pow(2, 3);   // 8
2 ** 3;           // 8 (équivalent)

Math.pow(5, 2);   // 25       // carré
Math.pow(9, 0.5); // 3        // racine carrée
Math.pow(27, 1/3);// 3        // racine cubique
```

## `Math.min()` - plus petite valeur

Retourne la **plus petite** valeur parmi les arguments.
Pour un **tableau**, utilise l’**opérateur spread**.

```javascript
Math.min(3, -1, 7);       // -1

const arr = [4, 1, 9];
Math.min(...arr);         // 1
```

## `Math.max()` - plus grande valeur

Retourne la **plus grande** valeur parmi les arguments.
Pour un **tableau**, utilise l’**opérateur spread**.

```javascript
Math.max(3, -1, 7);      // 7

const arr = [4, 1, 9];
Math.max(...arr);        // 9
```

## `Math.ceil()` - arrondir à la prochaine valeur entière la plus proche

Renvoie le **plus petit entier ≥ x** (arrondi vers le haut, vers **+∞**).

```javascript
Math.ceil(2.01);   // 3
Math.ceil(3);      // 3
Math.ceil(-1.1);   // -1

// Exemple courant : calcul de pages
const total = 53, parPage = 10;
const pages = Math.ceil(total / parPage); // 6
```


## `Math.floor()` - arrondir à la précédente valeur entière la plus proche

Renvoie le **plus grand entier ≤ x** (arrondi vers le bas, vers **-∞**).

```javascript
Math.floor(2.99);  // 2
Math.floor(3);     // 3
Math.floor(-1.1);  // -2

// Ex. discretiser un nombre en index
const x = 4.7;
const index = Math.floor(x); // 4
```

## `Math.round()` - arrondir à la valeur entière la plus proche

Arrondit au **plus proche entier** ; les valeurs en **.5** vont vers **+∞**.

```javascript
Math.round(2.49); // 2
Math.round(2.5);  // 3
Math.round(-1.1); // -1
Math.round(-1.5); // -1
Math.round(-1.6); // -2
```

## `Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre

Retire la partie **décimale** (tronque), **vers 0**.

```javascript
Math.trunc(3.9);    // 3
Math.trunc(-3.9);   // -3
Math.trunc(3);      // 3
Math.trunc('42.7'); // 42  (conversion implicite)

// Différence avec floor pour les négatifs
Math.trunc(-1.9);   // -1
Math.floor(-1.9);   // -2
```

## `Math.sqrt()` - la raçine carrée d'un nombre

Retourne la **racine carrée** de `x` (résultat ≥ 0).
Si `x < 0` → `NaN`. Équivalent possible : `x ** 0.5`.

```javascript
Math.sqrt(9);     // 3
Math.sqrt(2);     // 1.4142135623...
Math.sqrt(0);     // 0
Math.sqrt(-1);    // NaN

// Distance 2D (théorème de Pythagore)
const dx = 6, dy = 8;
const dist = Math.sqrt(dx*dx + dy*dy); // 10
```

## `Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)

Renvoie un **flottant** `x` tel que `0 ≤ x < 1`.
(Pas sécurisé pour la crypto — pour ça, utiliser `crypto.getRandomValues`.)

```javascript
Math.random(); // ex: 0.7321...

// Entier dans [min, max] (inclus)
const randInt = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;

// Tirer un élément au hasard
const item = arr[Math.floor(Math.random() * arr.length)];

// Pile ou face (booléen)
const coin = Math.random() < 0.5;
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# JSON

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON)

## `JSON.stringify()` - transformer un objet Javascript en JSON

Convertit une **valeur JS** en **chaîne JSON**.
Syntaxe : `JSON.stringify(value, replacer?, space?)`

```javascript
// Basique
const obj = { nom: 'Ada', age: 28 };
const json = JSON.stringify(obj);     // '{"nom":"Ada","age":28}'

// Avec indentation (pretty-print)
JSON.stringify(obj, null, 2);
/*
{
  "nom": "Ada",
  "age": 28
}
*/

// Filtrer des clés (replacer = tableau)
JSON.stringify(obj, ['nom']);         // '{"nom":"Ada"}'

// Transformer des valeurs (replacer = fonction)
JSON.stringify({ mdp: 'secret', x: 3.14159 }, (k, v) =>
  k === 'mdp' ? '***' : v
); // '{"mdp":"***","x":3.14159}'
```

> `undefined`, `function` et `Symbol` : **ignorés** dans les objets, deviennent `null` dans les tableaux.
> Les `Date` sont sérialisées au format **ISO** (ex. `"2025-06-06T13:23:42.123Z"`).


## `JSON.parse()` - transformer du JSON en objet Javascript

Convertit une **chaîne JSON** en **valeur JS**.
Syntaxe : `JSON.parse(text, reviver?)`

```javascript
// Basique
const s = '{"nom":"Ada","age":28,"tags":["js","fp"]}';
const data = JSON.parse(s);
data.nom; // "Ada"
```

```javascript
// Avec "reviver" (ex : convertir les dates ISO en objets Date)
const s = '{"created":"2025-06-06T13:23:42.123Z"}';
const obj = JSON.parse(s, (k, v) =>
  (typeof v === 'string' && /^\d{4}-\d{2}-\d{2}T/.test(v)) ? new Date(v) : v
);
obj.created instanceof Date; // true
```

```javascript
// Gérer les erreurs de parsing
try {
  JSON.parse('pas du json');
} catch (e) {
  console.error('JSON invalide:', e.message);
}
```

> JSON ≠ JS : guillemets **doubles**, **pas** de commentaires, ni `undefined/NaN/Infinity`.

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Chaînes de caractères

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String)

## `split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau

Sépare une **chaîne** en **tableau** selon un **séparateur** (texte ou **RegExp**).
Argument optionnel `limit` = nombre max d’éléments.

```javascript
"1,2,3".split(",");            // ["1","2","3"]
"a-b-c-d".split("-", 2);       // ["a","b"]  (limit)

const txt = "ligne1\nligne2\nligne3";
txt.split("\n");               // ["ligne1","ligne2","ligne3"]

"  a   b   c  ".trim().split(/\s+/); // ["a","b","c"]  (espaces multiples)

"a,,b,".split(",").filter(Boolean);  // ["a","b"]  (sans vides)
"hello".split("");                   // ["h","e","l","l","o"]
```

## `trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)

Suppriment les **espaces blancs** (espaces, tabulations, retours ligne) en **bordure** de chaîne.

* `trim()` : début **et** fin
* `trimStart()` : début uniquement *(alias historique : `trimLeft()`)*
* `trimEnd()` : fin uniquement *(alias historique : `trimRight()`)*

```javascript
"  hello  ".trim();        // "hello"
"\n\tok \t".trimStart();   // "ok \t"
" done\n".trimEnd();       // " done"

["  a ", " b", "c  "].map(s => s.trim()); // ["a","b","c"]

// Attention : n'enlève rien AU MILIEU
" a  b ".trim();           // "a  b"
```

## `padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères

Complètent une **chaîne** jusqu’à une **longueur cible** en ajoutant des caractères au **début** (`padStart`) ou à la **fin** (`padEnd`).
Syntaxe : `str.padStart(len, pad?)` / `str.padEnd(len, pad?)`

```javascript
// Zéro-padding (numéro, date, etc.)
String(7).padStart(3, '0');      // "007"

// Alignement à droite / gauche
"42".padStart(5);                // "   42"
"42".padEnd(5);                  // "42   "

// Masquer un identifiant
"1234".padStart(16, '•');        // "••••••••••••1234"

// Colonnes fixes
["a", "bb", "ccc"].map(s => s.padEnd(5, ' '));
// ["a    ","bb   ","ccc  "]
```

> Si la chaîne est déjà **≥ longueur cible**, elle est renvoyée **inchangée**. `pad` par défaut = espace.


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

Affichent des messages avec un **niveau** (info, avertissement, erreur), **filtrables** dans les DevTools.
`warn` met en évidence en **jaune**, `error` en **rouge** (avec stack).

```javascript
console.info('Démarré en %d ms', 123);

const quota = 92;
console.warn('Quota élevé : %s%%', quota);

const status = 500, url = '/api/data';
console.error('Échec requête', { status, url });

// Bon à savoir : on peut logguer des objets directement
console.info({ user: { id: 1, nom: 'Ada' } });
```

## `console.table()` - Afficher tout un tableau ou un objet sur la console

Affiche des **données tabulaires** de façon lisible (tableaux, tableaux d’objets, objets).

```javascript
// Tableau d’objets
const users = [
  { id: 1, nom: 'Ada', score: 42 },
  { id: 2, nom: 'Linus', score: 37 },
];
console.table(users);

// Sélection de colonnes
console.table(users, ['id', 'score']);

// Objet d’objets
const mesures = {
  a: { x: 1, y: 2 },
  b: { x: 3, y: 4 },
};
console.table(mesures);

// Tableau simple
console.table([10, 20, 30]); // colonnes: (index), value
```


## `console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution

Crée un **chronomètre** nommé :

* `console.time(label)` démarre
* `console.timeLog(label, ...data?)` affiche le temps écoulé (sans arrêter)
* `console.timeEnd(label)` arrête et affiche le **total**

```javascript
console.time('build');
// ... code à mesurer ...
console.timeLog('build', 'après étape 1');
// ... autre travail ...
console.timeEnd('build'); // "build: 123.45 ms"
```

```javascript
// Label facultatif : "default"
console.time();
doSomething();
console.timeEnd(); // "default: 4.12 ms"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Tableaux

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array)

## `forEach` - parcourir les éléments d'un tableau

Exécute une **fonction** pour **chaque élément** du tableau (dans l’ordre).
Ne retourne rien (**`undefined`**), sert aux **effets de bord**.

```javascript
const arr = ['a', 'b', 'c'];

// (valeur, index, tableau)
arr.forEach((v, i) => {
  console.log(i, v);
});
// 0 'a'
// 1 'b'
// 2 'c'

// Exemple : somme
let somme = 0;
[1, 2, 3].forEach(n => { somme += n; }); // 6
```

## `entries()` - parcourir les couples index/valeurs d'un tableau

Renvoie une **suite de paires** `[index, valeur]` pour chaque élément du tableau.
Utile pour **boucler** en ayant la **position** (0, 1, 2, …) **et** la **valeur**.

```javascript
const arr = ['a', 'b', 'c'];

// Parcours avec position + valeur
for (const [i, v] of arr.entries()) {
  console.log(i, v);
}
// 0 'a'
// 1 'b'
// 2 'c'

// Sans "déstructuration"
for (const pair of arr.entries()) {
  const i = pair[0];
  const v = pair[1];
  console.log(i, v);
}

// Obtenir un "vrai" tableau de paires
[...arr.entries()]; // [[0,'a'], [1,'b'], [2,'c']]
```

## `in` - parcourir les clés d'un tableau

Parcourt les **clés** d’un tableau, en tant que **chaînes**.

```javascript
const arr = ['a', 'b', 'c'];
for (const i in arr) {
  console.log(i, arr[i]); // 0 'a' / 1 'b' / 2 'c'
}
```

```javascript
// Trous ignorés
const a = [];
a[2] = 'x';
for (const i in a) console.log(i); // "2"
```

```javascript
// Attention : parcourt aussi les propriétés ajoutées
arr.extra = 99;
for (const k in arr) console.log(k); // "0","1","2","extra"
```

## `for...of` - parcourir les valeurs d'un tableau

Boucle directement sur les **valeurs** du tableau (dans l’ordre).

```javascript
const arr = ['a', 'b', 'c'];
for (const v of arr) {
  console.log(v); // 'a', 'b', 'c'
}
```

```javascript
// Besoin aussi de l’index ? Utilise entries()
for (const [i, v] of arr.entries()) {
  console.log(i, v); // 0 'a' / 1 'b' / 2 'c'
}
```

```javascript
// Fonctionne aussi avec les chaînes, Set, Map (leurs valeurs)
for (const ch of "hey") console.log(ch); // 'h','e','y'
```

## `find()` - premier élément qui satisfait une condition

Retourne la **première valeur** du tableau pour laquelle le **test** renvoie `true`, sinon `undefined`.
Signature : `arr.find((val, i, arr) => test, thisArg?)`

```javascript
[5, 12, 8, 130, 44].find(n => n > 10); // 12
[1, 2, 3].find(n => n > 5);             // undefined

const users = [
  { id: 1, nom: 'Ada' },
  { id: 2, nom: 'Linus' },
];
users.find(u => u.nom === 'Ada');       // { id: 1, nom: 'Ada' }
```

## `findIndex()` - premier index qui satisfait une condition

Retourne l’**index** du **premier** élément pour lequel le test renvoie `true`, sinon **`-1`**.
Signature : `arr.findIndex((val, i, arr) => test, thisArg?)`

```javascript
[5, 12, 8, 130, 44].findIndex(n => n > 10); // 1 (car 12)

// Sur objets
const users = [{id:1},{id:3},{id:5}];
users.findIndex(u => u.id === 3); // 1
users.findIndex(u => u.id === 2); // -1

// Supprimer le premier match
const i = users.findIndex(u => u.id === 3);
if (i !== -1) users.splice(i, 1);
```

## `indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond

Renvoient l’**index** de la **première** (`indexOf`) ou **dernière** (`lastIndexOf`) occurrence d’une valeur, sinon **`-1`**.
Signatures :
`arr.indexOf(val, fromIndex = 0)`
`arr.lastIndexOf(val, fromIndex = arr.length - 1)`

```javascript
[1, 2, 3, 2].indexOf(2);          // 1
[1, 2, 3, 2].indexOf(2, 2);       // 3 (à partir de l’index 2)

[1, 2, 3, 2].lastIndexOf(2);      // 3
['a','b','a'].lastIndexOf('a', 1);// 0 (en partant de 1 vers la gauche)

['x','y'].indexOf('z');           // -1
```

```javascript
// Comparaison stricte (===) et références
const a = { x: 1 };
[a, { x: 1 }].indexOf(a);         // 0
[a, { x: 1 }].indexOf({ x: 1 });  // -1 (objets différents)

// Cas NaN
[NaN].indexOf(NaN);               // -1
[NaN].includes(NaN);              // true (si besoin)
```

## `push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprimer au début/fin d’un tableau

**Mutent** le tableau :

* `push(x, ...)` : **ajoute à la fin**, retourne la **nouvelle longueur**
* `pop()` : **retire la fin**, retourne l’**élément retiré**
* `unshift(x, ...)` : **ajoute au début**, retourne la **nouvelle longueur**
* `shift()` : **retire le début**, retourne l’**élément retiré**

```javascript
const arr = [1, 2];

// Fin
arr.push(3);   // 3   (arr → [1,2,3])
arr.pop();     // 3   (arr → [1,2])

// Début
arr.unshift(0); // 3  (arr → [0,1,2])
arr.shift();    // 0  (arr → [1,2])
```

## `slice()` - ne conserver que certaines lignes d'un tableau

Retourne une **copie** d’une portion du tableau, **sans le modifier**.
`arr.slice(début, fin?)` — `début` inclus, `fin` **exclu**. Indices négatifs = à partir de la fin.

```javascript
const arr = [0, 1, 2, 3, 4];

arr.slice(1, 4);   // [1, 2, 3]
arr.slice(2);      // [2, 3, 4]
arr.slice(-2);     // [3, 4]

// Cloner un tableau
const copie = arr.slice(); // [0,1,2,3,4]

// Pagination simple
const page = (items, p, n) => items.slice((p-1)*n, p*n);
```

## `splice()` - supprimer/insérer/remplacer des valeurs dans un tableau

**Modifie** le tableau en place.
Signature : `arr.splice(début, deleteCount, ...élémentsÀInsérer)`
Retourne un **tableau des éléments supprimés**.

```javascript
// Supprimer
const a = [0,1,2,3,4];
const suppr = a.splice(2, 1);   // supprime 1 élément à partir de l’index 2
// a → [0,1,3,4], suppr → [2]

// Insérer (sans supprimer)
const b = [0,1,2,3];
b.splice(2, 0, 'x', 'y');       // insère à l’index 2
// b → [0,1,'x','y',2,3]

// Remplacer
const c = [0,1,2,3];
c.splice(1, 2, 'A');            // remplace 1 et 2 par 'A'
// c → [0,'A',3]

// Indices négatifs = depuis la fin
const d = [10,20,30,40];
d.splice(-2, 1);                // supprime 30
// d → [10,20,40]

// Vider un tableau
const e = [1,2,3];
e.splice(0);                    // e → []
```

## `concat()` - joindre deux tableaux

Retourne un **nouveau tableau** en **chaînant** des tableaux et/ou valeurs.
Ne **modifie pas** les originaux (équiv. courant : l’opérateur **spread**).

```javascript
const a = [1, 2];
const b = [3, 4];

a.concat(b);            // [1, 2, 3, 4]
a.concat(0, b, 5);      // [1, 2, 0, 3, 4, 5]
[].concat(a, b);        // [1, 2, 3, 4] (clonage simple avec concat)

const nested = [1, [2, 3]];
nested.concat([4, [5]]); // [1, [2,3], 4, [5]]  (pas d’aplatissement profond)

// Alternative spread
[...a, ...b];           // [1, 2, 3, 4]
```

## `join()` - joindre des chaînes de caractères

Rassemble les **éléments d’un tableau** en **une seule chaîne**.
Syntaxe : `arr.join(séparateur?)` — séparateur par défaut **","**.

```javascript
['a','b','c'].join();         // "a,b,c"
['a','b','c'].join(' - ');    // "a - b - c"
[1,2,3].join('');             // "123" (sans séparateur)
['usr','local','bin'].join('/'); // "usr/local/bin"

// Valeurs spéciales et "trous"
[null, undefined, ''].join('|'); // "||"
[1, , 3].join('-');              // "1--3"
```

## `keys()` et `values()` - les clés/valeurs d'un objet

`Object.keys(obj)` renvoie un **tableau des clés** propres et énumérables.
`Object.values(obj)` renvoie le **tableau des valeurs** correspondantes. (Pas les propriétés du **prototype**.)

```javascript
const user = { id: 1, nom: 'Ada', actif: true };

Object.keys(user);   // ["id", "nom", "actif"]
Object.values(user); // [1, "Ada", true]

// Parcourir clés + valeurs
Object.keys(user).forEach(k => {
  console.log(k, user[k]);
});

// Avec un tableau (les indices deviennent des chaînes)
Object.keys(['a','b']);   // ["0","1"]
Object.values(['a','b']); // ["a","b"]
```

> Astuce : pour des **couples [clé, valeur]**, utilise aussi `Object.entries(obj)`.

## `includes()` - vérifier si une valeur est présente dans un tableau

Renvoie **true/false** si le tableau **contient** la valeur.
Syntaxe : `arr.includes(val, fromIndex = 0)` (indices négatifs acceptés).

```javascript
[1, 2, 3].includes(2);        // true
[1, 2, 3].includes(4);        // false
['a','b','c'].includes('a',1);// false (cherche dès l’index 1)
['a','b','c'].includes('c',-1);// true (depuis la fin)

// Cas spéciaux
[NaN].includes(NaN);          // true
const o = {x:1};
[o].includes(o);              // true
[{x:1}].includes({x:1});      // false (références différentes)
```

## `every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau

* `every(test)` → **true si tous** les éléments passent le test.
* `some(test)` → **true si au moins un** élément passe le test.
  S’arrêtent **dès que le résultat est connu**.

```javascript
const nums = [2, 4, 6];

nums.every(n => n % 2 === 0);  // true  (tous pairs)
nums.some(n => n < 0);         // false (aucun négatif)

// Valider un formulaire : tous non vides ?
['nom','email','pwd'].every(k => form[k]?.trim());

// Vérifier si une extension est autorisée
const allowed = ['jpg','png','gif'];
allowed.some(ext => fileName.endsWith('.' + ext)); // true/false

// Sous-ensemble : arr contient toutes les valeurs de req ?
const req = ['READ','WRITE'];
req.every(r => rights.includes(r)); // true/false
```

## `fill()` - remplir un tableau avec des valeurs

Remplit **en place** un tableau avec une valeur.
`arr.fill(val, début = 0, fin = arr.length)` — `début` inclus, `fin` **exclu** (indices négatifs ok).

```javascript
// Basique
Array(5).fill(0);                 // [0,0,0,0,0]

// Plage ciblée
const a = [1,2,3,4];
a.fill(9, 1, 3);                  // [1,9,9,4]

// Depuis la fin
[1,2,3,4].fill(7, -2);            // [1,2,7,7]

// Retourne le même tableau (mutation)
const b = [1,2,3];
const r = b.fill(8);              // b === r → true
```

## `flat()` - aplatir un tableau

Crée un **nouveau tableau** en aplatissant les **sous-tableaux** jusqu’à une **profondeur** donnée.
Syntaxe : `arr.flat(depth = 1)`

```javascript
[1, [2, 3], [4]].flat();           // [1, 2, 3, 4]
[1, [2, [3, [4]]]].flat(2);        // [1, 2, 3, [4]]
[1, [2, [3, [4]]]].flat(Infinity); // [1, 2, 3, 4]

// Les "trous" sont supprimés
[1, , [2, , 3]].flat();            // [1, 2, 3]
```

## `sort()` - pour trier un tableau

**Trie en place** (modifie l’original).
Par défaut : **ordre lexicographique** (comme des chaînes).
Pour un tri **numérique** ou **personnalisé**, fournis une fonction de comparaison.

```javascript
// Par défaut (lexicographique)
[3, 20, 100, 4].sort();                // [100, 20, 3, 4]

// Numérique (croissant / décroissant)
[3, 20, 100, 4].sort((a, b) => a - b); // [3, 4, 20, 100]
[3, 20, 100, 4].sort((a, b) => b - a); // [100, 20, 4, 3]

// Objets : trier par propriété
const users = [{age: 30},{age: 20},{age: 25}];
users.sort((a, b) => a.age - b.age);   // [{20},{25},{30}]

// Chaînes avec accents (locale)
['é', 'e', 'è'].sort((a,b) => a.localeCompare(b, 'fr'));
```

## `map()` - tableau avec les résultats d'une fonction

Applique une **fonction** à chaque élément et **retourne un nouveau tableau**.
Ne **modifie pas** l’original. Longueur **inchangée**.
Signature : `arr.map((val, i, arr) => nouveauVal, thisArg?)`

```javascript
// Transformer des nombres
[1, 2, 3].map(n => n * 2);           // [2, 4, 6]

// Extraire une propriété
const users = [{nom:'Ada'}, {nom:'Linus'}];
users.map(u => u.nom);               // ["Ada", "Linus"]

// Utiliser l’index
['a','b','c'].map((v,i) => `${i}:${v}`); // ["0:a","1:b","2:c"]

// Conversion pratique
['1','2','3'].map(Number);           // [1, 2, 3]
```

## `filter()` - tableau avec les éléments passant un test

Garde **uniquement** les éléments pour lesquels le **test** retourne `true`.
Retourne un **nouveau tableau**, ne **modifie pas** l’original.
Signature : `arr.filter((val, i, arr) => condition, thisArg?)`

```javascript
// Garder les nombres > 10
[5, 12, 8, 130, 44].filter(n => n > 10); // [12, 130, 44]

// Filtrer des objets (ex : actifs)
const users = [{actif:true},{actif:false},{actif:true}];
users.filter(u => u.actif); // [{actif:true},{actif:true}]

// Retirer les valeurs "falsy" (0, '', null, undefined, NaN)
['a', '', null, 'b'].filter(Boolean); // ["a", "b"]
```

## `groupBy()` - regroupe les éléments d'un tableau selon une règle

Groupe les éléments **par clé** calculée à partir d’une fonction.
(En environnements modernes : `array.group(fn)` / `array.groupToMap(fn)`. Sinon, utilise `reduce`.)

```javascript
// Exemple : grouper par ville
const people = [
  { nom: 'Ana',  ville: 'Lyon'  },
  { nom: 'Ben',  ville: 'Lyon'  },
  { nom: 'Eli',  ville: 'Paris' },
];

// Si dispo
people.group(p => p.ville);
// { Lyon: [ {Ana}, {Ben} ], Paris: [ {Eli} ] }

people.groupToMap(p => p.ville);
// Map(2) { 'Lyon' => [ {Ana}, {Ben} ], 'Paris' => [ {Eli} ] }
```

```javascript
// Variante compatible partout (reduce)
const byVille = people.reduce((acc, p) => {
  (acc[p.ville] ??= []).push(p);
  return acc;
}, {});
// { Lyon: [ ... ], Paris: [ ... ] }
```

```javascript
// Autre exemple : pair / impair
[1,2,3,4,5].group?.(n => (n % 2 ? 'impair' : 'pair'))
// { pair: [2,4], impair: [1,3,5] }
```

## `flatMap()` - chaînage de map() et flat()

Fait un **map** puis aplati d’**un niveau** en **une seule passe**.
Signature : `arr.flatMap((val, i, arr) => valeurOuTableau)`

```javascript
// 1) Décomposer puis aplatir
['a b', 'c d'].flatMap(s => s.split(' ')); 
// ["a","b","c","d"]

// 2) Transformer en multipliant les éléments
[1, 2, 3].flatMap(n => [n, n * 2]);
// [1, 2, 2, 4, 3, 6]

// 3) Filtrer en retournant [] pour exclure
[1, 2, 3, 4].flatMap(n => n % 2 ? [n] : []);
// [1, 3]
```

## `reduce()` et `reduceRight()` - réduire un tableau à une seule valeur

Appliquent une **fonction d’accumulation** pour produire **une valeur unique**.

* `reduce` : de **gauche → droite**
* `reduceRight` : de **droite → gauche**
  Signature : `arr.reduce((acc, val, i, arr) => newAcc, init?)`

```javascript
// Somme
[1, 2, 3, 4].reduce((acc, n) => acc + n, 0); // 10

// Max
[5, 1, 9, 3].reduce((m, n) => n > m ? n : m, -Infinity); // 9

// Comptage par valeur (fréquences)
['a','b','a','c','b','a'].reduce((map, k) => {
  map[k] = (map[k] || 0) + 1;
  return map;
}, {}); // { a:3, b:2, c:1 }

// reduceRight : sens inverse
['a','b','c'].reduceRight((acc, v) => acc + v, ''); // "cba"
```

## `reverse()` - inverser l'ordre du tableau

Inverse **en place** l’ordre des éléments et retourne **le même tableau** (mutation).

```javascript
const a = [1, 2, 3];
a.reverse();        // [3, 2, 1]
a;                  // [3, 2, 1]  (modifié)
```

```javascript
// Sans muter l’original
const b = [1, 2, 3];
const r = b.slice().reverse(); // [3,2,1]
```

```javascript
// Alternative moderne (si dispo) : ne mute pas
[1, 2, 3].toReversed(); // [3,2,1]
```

```javascript
// Inverser une chaîne
"salut".split('').reverse().join(''); // "tulas"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Techniques

## ``(backticks) - pour des expressions intelligentes

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `new Set()` - pour supprimer les doublons

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
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
(function(){ ... })()
```

ou

```javascript
(() => { ... })()
```

# Conclusion

> Votre conclusion avec les éléments usuels
