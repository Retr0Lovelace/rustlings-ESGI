## variables6.rs

```rust
# Chapitre 1: Variables

Le programme précédent dans le chapitre sur les variables ne compilait pas car le type de variable n'avait pas été défini. J'ai donc simplement précisé le type "NUMBER: i32" afin que le programme puisse compiler.
```

## functions5.rs

```rust
# Chapitre 2: Fonctions

Dans le chapitre sur les fonctions, le problème venait du fait que le résultat de num * num n'était pas retourné en fin de programme. J'ai donc retiré le ";" après l'opération afin que le résultat puisse être retourné.
```

## if3.rs

```rust
# Chapitre 3: Conditions

Dans le chapitre sur les conditions, le programme ne compilait pas car les "identifiants" étaient attendus en entier, mais la condition proposait le string "unknown". J'ai remplacé "unknown" par 4, car il était présent dans la condition suivante, dans le cas où l'identifiant serait différent de 1, 2 ou 3.
```

## primitive_types6.rs

```rust
# Chapitre 4: Types primitifs

Dans ce chapitre, il est demandé de récupérer la seconde valeur présente dans le tuple. La position des valeurs commençant à 0, il fallait donc récupérer la valeur à l'emplacement 1 du tuple. Pour ce faire, on va récupérer la valeur de la façon suivante: `numbers.1`.
```

## vecs2.rs

```rust
# Chapitre 5: Vecteurs

Il nous est demandé ici de multiplier par 2 les éléments présents dans le vecteur ayant le nom "v". Il va donc falloir le faire de deux manières différentes. La première manière consiste à créer une ligne effectuant le calcul sans faire de retour direct, car le `.iter_mut()` va se charger de changer les valeurs du vecteur. La deuxième méthode consiste simplement à retourner le résultat de la multiplication par 2, qui va remplacer l'ancienne valeur.
```

## move_semantics6.rs

```rust
# Chapitre 6: Sémantique de déplacement

Dans ce programme, le code ne pouvait pas compiler car la relation d'ownership n'était pas correctement appliquée. La fonction "string_uppercase" devant récupérer l'ownership, j'ai commencé par supprimer les "&" présents, car cela indiquait que l'on empruntait la valeur à une autre fonction. Ensuite, j'ai retiré également le symbole "&" à la ligne 13 afin de montrer que la fonction possède la variable. Ensuite, j'ai fait la procédure inverse avec la fonction "get_char" afin que celle-ci emprunte "data" à la fonction "string_uppercase".
```

## structs3.rs

```rust
# Chapitre 7: Structures

Dans ce cas, le code n'est pas terminé et il nous est demandé de compléter les fonctions qui définiront si notre colis est envoyé à l'international ou non, et à combien vont s'élever les frais d'envoi. On va faire appel à "&self" car le code étant présent dans "impl package", le self fait référence au colis. On va donc vérifier si le colis a le même pays d'envoi et de réception, et si oui, le colis n'est pas international. Sinon, cela signifie qu'il est bien envoyé à l'international. Ensuite, dans l'autre fonction, on va tout simplement faire la multiplication du poids du colis en grammes par le prix de l'envoi par gramme du colis, soit "3 * <poids du colis>".
```

## enums3.rs

```rust
# Chapitre 8: Énumérations

Dans ce code, on va effectuer une énumération des fonctions présentes ci-dessus. Pour ce faire, on va leur attribuer une expression à chacune. Pour les expressions, je me suis fié aux "state.process" présents plus bas dans le code afin de les nommer. Ensuite, je les ai associées avec leur fonction correspondante, en prenant bien soin de suivre le conseil dans le "TODO" en ajoutant des parenthèses lorsque je fais appel à un tuple (ce qui fut le cas pour le echo et le move_position).
```

## strings4.rs

```rust
# Chapitre 9: Chaînes de caractères

Dans ce cas, on va utiliser les fonctions string et string_slice en fonction de ce que l'on souhaite faire de la donnée. Si on veut récupérer seulement une partie de la chaîne de caractères, on va utiliser string_slice. En revanche, si on souhaite posséder, créer ou modifier la chaîne de caractères, on utilisera string.
```

## modules3.rs

```rust
# Chapitre 10: Modules

Dans ce cas, le code ne compilait pas car SystemTime et UNIX_EPOCH n'avaient pas été importés dans le code. Il a fallu donc, en suivant les informations données par l'énoncé, ajouter les deux avec la ligne suivante : `use std::time::{SystemTime, UNIX_EPOCH};`.
```

## hashmaps3.rs

```rust
# Chapitre 11: Hashmaps

Dans le code, il est demandé de rajouter des lignes afin de compter le score entre 2 équipes. On va donc utiliser le hashmap afin de faciliter le stockage des valeurs "goals_scored" et "goals_conceded". Ensuite, on va effectuer un déréférencement avec le symbole * pour pouvoir modifier les valeurs dans le hashmap.
```

## options3.rs

```rust
# Chapitre 12: Options

Je n'ai pas directement remarqué, car pour moi le code devait s'exécuter normalement. Cependant, le problème venait du fait que le match "y" ne précisait pas qu'il souhaitait récupérer la valeur de la variable créée au-dessus à l'aide de l'esperluette.
```

## generics2.rs

```rust
# Chapitre 13: Génériques

Après des recherches, je me suis aperçu que pour supporter des résultats de n'importe quel type, il fallait remplacer les "u32" par "T". À l'aide des erreurs remontées par Rust, j'ai ensuite ajouté les `<T>` là où ils devaient être, et le code a pu compiler.
```

## errors6.rs

```rust
# Chapitre 14: Erreurs

Dans cet exercice, on doit commencer par créer une fonction permettant de bien différencier les `parseIntError` des `CreationError`. Pour ce faire, j'ai adapté la fonction `from_creation` de manière à faire la même chose avec la fonction `from

_parseint`. Ensuite, il a fallu préciser dans quel cas l'erreur apparaît dans la fonction `parse_pos_nonzero`.
```

## traits5.rs

```rust
# Chapitre 15: Traits

Dans ce morceau de code, il est nécessaire d'ajouter `impl SomeTrait + OtherTrait`. En effet, si on ne le fait pas, le compilateur ne sait pas interpréter le type de "Item".
```

## lifetimes3.rs

```rust
# Chapitre 16: Durée de vie

Dans cet énoncé, il nous est demandé d'appliquer les lifetimes aux structs qui sont référencées. J'ai donc appliqué la même chose que pour les exercices précédents, mais sur la structure. J'ai donc ajouté le `<'duree>` afin de définir la durée de vie des références, puis je l'ai appliqué à "author" et "title" avec le `&'duree`.
```

## tests4.rs

```rust
# Chapitre 17: Tests

Ici, le code ne compile pas car il faut commencer par tester la hauteur et la largeur du rectangle dans les lignes 31 et 32 avec `assert_eq!`. Ensuite, le code n'étant pas doté de gestion des erreurs, il nous manque une réponse en cas d'erreur. C'est à ce moment que l'on va fournir `#[should_panic]` afin que les fonctions devant retourner une erreur si le cas se présente puissent provoquer une panique.
```
