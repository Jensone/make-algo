### Exercice 1: Inversion de Chaîne

Objectif: Inverser une chaîne de caractères.

- Entrée: "Bonjour"
- Sortie attendue: "ruojnoB"

Solution:

```bash
DÉBUT ALGORITHME
    chaine = "Bonjour"
    inversée = ""
    POUR CHAQUE caractère DANS chaine
        inversée = caractère + inversée
    FIN POUR
    AFFICHER inversée
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$chaine = "Bonjour";
$inversee = "";
for ($i = 0; $i < 7; $i++) {
    $inversee = $chaine[$i] . $inversee;
}
echo $inversee;
?>
```

`strlen()` est une fonction PHP qui retourne la longueur d'une chaîne de caractères.

---

### Exercice 2: Somme des Nombres

Objectif: Calculer la somme de tous les nombres jusqu'à un nombre donné.

- Entrée: 5
- Sortie attendue: 15 (1+2+3+4+5)

Solution:

```bash
DÉBUT ALGORITHME
    nombre = 5
    somme = 0
    POUR i DE 1 À nombre
        somme = somme + i
    FIN POUR
    AFFICHER somme
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$nombre = 5;
$somme = 0;
for ($i = 1; $i <= $nombre; $i++) {
    $somme = $somme + $i;
}
echo $somme;
?>
```

---

### ### Exercice 3: Factorielle

Objectif: Trouver la factorielle d'un nombre.

- Entrée: 4
- Sortie attendue: 24 (1*2*3\*4)

Solution:

```bash
DÉBUT ALGORITHME
    nombre = 4
    factorielle = 1
    POUR i DE 1 À nombre
        factorielle = factorielle * i
    FIN POUR
    AFFICHER factorielle
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$nombre = 4;
$factorielle = 1;
for ($i = 1; $i <= $nombre; $i++) {
    $factorielle = $factorielle * $i;
}
echo $factorielle;
?>
```

Petit rappel de mathématiques, "factorielle" est le produit des nombres entiers positifs inférieurs ou égaux à N. Par exemple, la factorielle de 4 est 1*2*3\*4 = 24. En mathématiques, on écrit 4! = 24.

C'est juste pour l'exercice, en programmation, on n'a pas besoin d'être bon en mathématiques pour coder.

---

### Exercice 4: Trouver le Plus Grand Nombre

Objectif: Trouver le plus grand nombre dans un tableau.

- Entrée: [3, 7, 2, 5]
- Sortie attendue: 7

Solution:

```bash
DÉBUT ALGORITHME
    tableau = [3, 7, 2, 5]
    plusGrand = tableau[0]
    POUR CHAQUE nombre DANS tableau
        SI nombre > plusGrand
            plusGrand = nombre
        FIN SI
    FIN POUR
    AFFICHER plusGrand
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$tableau = [3, 7, 2, 5];
$plusGrand = $tableau[0];
for ($i = 0; $i < count($tableau); $i++) {
    if ($tableau[$i] > $plusGrand) {
        $plusGrand = $tableau[$i];
    }
}
echo $plusGrand;
?>
```

`count()` est une fonction PHP qui retourne le nombre d'éléments dans un tableau.

---

### Exercice 5: FizzBuzz

Objectif: Pour chaque nombre de 1 à N, imprimer "Fizz" si le nombre est divisible par 3, "Buzz" s'il est divisible par 5, "FizzBuzz" s'il est divisible par les deux, sinon imprimer le nombre.

- Entrée: 5
- Sortie attendue: 1, 2, Fizz, 4, Buzz

Solution:

```bash
DÉBUT ALGORITHME
    nombre = 5
    POUR i DE 1 À nombre
        SI i % 3 == 0 ET i % 5 == 0
            AFFICHER "FizzBuzz"
        SINON SI i % 3 == 0
            AFFICHER "Fizz"
        SINON SI i % 5 == 0
            AFFICHER "Buzz"
        SINON
            AFFICHER i
        FIN SI
    FIN POUR
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$nombre = 5;
for ($i = 1; $i <= $nombre; $i++) {
    if ($i % 3 == 0 && $i % 5 == 0) {
        echo "FizzBuzz";
    } else if ($i % 3 == 0) {
        echo "Fizz";
    } else if ($i % 5 == 0) {
        echo "Buzz";
    } else {
        echo $i;
    }
}
?>
```

`%` est l'opérateur modulo, il retourne le reste de la division entière.

Version factorisée:

```php
<?php
$nombre = 5;
for ($i = 1; $i <= $nombre; $i++) {
    $output = "";
    if ($i % 3 == 0) {
        $output .= "Fizz";
    }
    if ($i % 5 == 0) {
        $output .= "Buzz";
    }
    echo $output ?: $i;
}
?>
```

`?:` est l'opérateur ternaire, il retourne la première expression si elle est vraie, sinon la deuxième.

---

### Exercice 6: Compter les Voyelles

Objectif: Compter le nombre de voyelles dans une chaîne.

- Entrée: "Algorithmique"
- Sortie attendue: 5

Solution:

```bash
DÉBUT ALGORITHME
    chaine = "Algorithmique"
    voyelles = ["a", "e", "i", "o", "u", "y"]
    nombreVoyelles = 0
    POUR CHAQUE caractère DANS chaine
        SI caractère EST DANS voyelles
            nombreVoyelles = nombreVoyelles + 1
        FIN SI
    FIN POUR
    AFFICHER nombreVoyelles
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$chaine = "Algorithmique";
$voyelles = ["a", "e", "i", "o", "u", "y"];
$nombreVoyelles = 0;
for ($i = 0; $i < strlen($chaine); $i++) {
    if (in_array($chaine[$i], $voyelles)) {
        $nombreVoyelles++;
    }
}
echo $nombreVoyelles;
?>
```

`in_array()` est une fonction PHP qui retourne vrai si un élément est présent dans un tableau.

---

### Exercice 7: Palindrome

Objectif: Vérifier si une chaîne est un palindrome.

- Entrée: "radar"
- Sortie attendue: Vrai

Solution:

```bash
DÉBUT ALGORITHME
    chaine = "radar"
    inversée = ""
    POUR CHAQUE caractère DANS chaine
        inversée = caractère + inversée
    FIN POUR
    SI chaine == inversée
        AFFICHER Vrai
    SINON
        AFFICHER Faux
    FIN SI
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$chaine = "radar";
$inversee = "";
for ($i = 0; $i < strlen($chaine); $i++) {
    $inversee = $chaine[$i] . $inversee;
}
if ($chaine == $inversee) {
    echo "Vrai";
} else {
    echo "Faux";
}
?>
```

---

### Exercice 8: Trouver les Éléments Communs

Objectif: Trouver les éléments communs entre deux tableaux.

- Entrée: [1, 2, 3], [2, 3, 4]
- Sortie attendue: [2, 3]

Solution:

```bash
DÉBUT ALGORITHME
    tableau1 = [1, 2, 3]
    tableau2 = [2, 3, 4]
    communs = []
    POUR CHAQUE nombre1 DANS tableau1
        POUR CHAQUE nombre2 DANS tableau2
            SI nombre1 == nombre2
                communs[] = nombre1
            FIN SI
        FIN POUR
    FIN POUR
    AFFICHER communs
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$tableau1 = [1, 2, 3];
$tableau2 = [2, 3, 4];
$communs = [];
for ($i = 0; $i < count($tableau1); $i++) {
    for ($j = 0; $j < count($tableau2); $j++) {
        if ($tableau1[$i] == $tableau2[$j]) {
            $communs[] = $tableau1[$i];
        }
    }
}
print_r($communs);
?>
```

`print_r()` est une fonction PHP qui affiche le contenu d'un tableau.

---

### Exercice 9: Nombre Premiers

Objectif: Générer une liste de nombres premiers jusqu'à un certain nombre.

- Entrée: 10
- Sortie attendue: [2, 3, 5, 7]

Solution:

```bash
DÉBUT ALGORITHME
    nombre = 10
    premiers = []
    POUR i DE 2 À nombre
        estPremier = Vrai
        POUR j DE 2 À i
            SI i % j == 0 ET i != j
                estPremier = Faux
            FIN SI
        FIN POUR
        SI estPremier
            premiers[] = i
        FIN SI
    FIN POUR
    AFFICHER premiers
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$nombre = 10;
$premiers = [];
for ($i = 2; $i <= $nombre; $i++) {
    $estPremier = true;
    for ($j = 2; $j < $i; $j++) {
        if ($i % $j == 0) {
            $estPremier = false;
        }
    }
    if ($estPremier) {
        $premiers[] = $i;
    }
}
print_r($premiers);
?>
```

Vous remarquerez que pour la boucle imbriquée le nom de la variable est `$j` et non `$i`. C'est une bonne pratique de nommer les variables de boucle avec des lettres différentes pour éviter les confusions.

---

### Exercice 10: Fibonacci

Objectif: Générer une série Fibonacci jusqu'au N-ième terme.

- Entrée: 5
- Sortie attendue: [0, 1, 1, 2, 3]

Solution:

```bash
DÉBUT ALGORITHME
    nombre = 5
    fibonacci = [0, 1]
    POUR i DE 2 À nombre
        fibonacci[] = fibonacci[i-1] + fibonacci[i-2]
    FIN POUR
    AFFICHER fibonacci
FIN ALGORITHME
```

Testez en PHP:

```php
<?php
$nombre = 5;
$fibonacci = [0, 1];
for ($i = 2; $i <= $nombre; $i++) {
    $fibonacci[] = $fibonacci[$i-1] + $fibonacci[$i-2];
}
print_r($fibonacci);
```

---

Voilà pour les exercices d'algorithmique. Vous pouvez les tester en PHP ou dans le langage de votre choix. Petit rappel, il est important de comprendre les concepts de base de la programmation avant de se lancer dans un langage de programmation. C'est comme apprendre à conduire une voiture, il faut d'abord comprendre le fonctionnement d'une voiture avant de conduire une voiture spécifique.

Le but d'un algo est de résoudre un problème, pas de coder. Lorsqu'on code, on doit d'abord comprendre le problème, puis trouver une solution, et enfin coder la solution. Coder c'est faire la traduction entre le langage humain et le langage machine. On appelle cela faire de l'implémentation, dans certain cas on peut être amené à faire de l'optimisation, c'est-à-dire améliorer la solution pour qu'elle soit plus rapide ou plus efficace. Cette dernière étape (factorisation) est optionnelle, il faut d'abord avoir une solution qui fonctionne.

Happy coding! 🤖
