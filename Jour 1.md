# Ruby Jour 1

## Ressources

- https://www.ruby-lang.org/fr/about/
- https://www.ruby-lang.org/fr/documentation/quickstart/
- https://www.ruby-lang.org/fr/documentation/ruby-from-other-languages/
- https://github.com/jbodah/ruby_for_experienced_developers
- https://try.ruby-lang.org/
- https://rubyapi.org/

## Exercices

### Exercice 0

Afficher `Hello World` sur la sortie standard.

### Exercice 1

Créer les variables suivantes :
- `title` qui aura pour valeur `"My article"`
- `likes` qui aura pour valeur `42`
- `status` qui pour valeur `:draft`
- `popular` qui aura pour valeur `true`
- `comments` qui aura pour valeur un array de string suivantes : `"Nice", "Not Bad", "Great"`.
- `data` qui sera un hash qui aura pour clés le nom de toutes les variables précédemment créées et en valeurs, les valeurs des variables correspondantes

Affichez les valeurs de ces variables sur la sortie standard.

### Exercice 2

- Créer une méthode `show_article` qui accepte 2 arguments `title` et `likes` et qui affichera la chaine de caractère suivante :
"{title} ({likes}) likes".
- Créer une méthode `popular?` qui accepte un argument entier `likes` et qui retourne true si likes est supérieur ou égal à 3 et false sinon.

- Créer une méthode `show_popular_articles` qui accepte un argument `articles` qui est un array d'articles et qui les affiche sous la forme "{title} ({likes}) likes" trié du plus populaire au moins populaire. Les articles au nombre de likes inférieur à 3 doivent être ignorés.
Un article sera représenté sous la forme d'un hash à la structure suivante : `{ title: "string", likes: 42 }`

### Exercice 3

- Créer une classe `Article` qui aura 2 variables d'instances `title` et `likes`. La valeur de `title` sera donné à l'initialisation de la classe, tandis que `likes` sera initialisé à 0

- L'attribut `title` doit pouvoir être retourné depuis une instance et l'attribut `likes` doit pouvoir être retourné et modifié.

- Implémenter une méthode `like` qui incrémentera l'attribut `likes` de 1. De la même manière, implémenter une méthode `dislike` qui décrémentera de 1 le nombre de likes.

- Implémenter une méthode `popular?` qui retournera un booléen déterminant si l'article est populaire ou non. Pour rappel, un article est populaire à partir de 3 likes ou plus.

### Exercice 4

- Charger le code de l'exercice précédent.

- Créer une classe `Comment` qui représentera un commentaire sur un article. Un Comment sera initialisée par son attribut `value` et sera lisible depuis l'extérieur de la classe.

Un commentaire pouvant être liké au même titre qu'un article, il est aussi caractérisé par un attribut `likes` et des méthodes `like`, `dislike` et `popular?` avec la même implémentation que sur la classe Article.

- Implémenter un module `Likeable` qui isolera ce comportement et l'inclure dans la classe `Article` et `Comment`

### Exercice 5

- Charger le code de l'exercice précédent.

- Un article peut être commenté. Implémenter une méthode `comment` qui acceptera la valeur du commentaire en argument et qui ajoutera une nouvelle instance de `Comment` (initialisée avec l'argument de la méthode) à une collection de commentaires `@comments`

- Un commentaire peut aussi être commenté. Isoler le comportement de commenter un objet et dans un module Commentable. L'inclure ensuite dans la classe Comment et Article

### Exercice 6

- Charger le code de l'exercice précédent.

- Implémenter une méthode `Article#review_comments` qui acceptera un block et qui l'appellera pour chaque élément `@comments`. La méthode ne doit pas renvoyer d'erreur en l'absence de block.

