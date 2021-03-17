Rapport TP1 – IFT3335

Étienne Beaulé (20120318), Nicolas Soriano (20127789), Anthony Uyende (20117140)

Le code pour chaque question est dans le fichier `sudokuN.py`, `N` étant le numéro de la question. C'est en Python3.
Note préliminaire: Les résultats sont différents pour du même code selon la question, dù à l'utilisation d'ordinateurs différents. Les résultats ayant une importance pour une question seront donc précisés dans celle-ci.

Questions 1 & 2
---------------

Le code fourni fonctionnait bien à part le chronomètre pour les tests qui était désuet et enlèvé à la version 3.3 de Python. On l'a donc remplacé. On a aussi remplacé le fichier de tests pour `100sudoku.txt`.

Sans modification substantielle (la question 1), tous les sudokus ont été réussis avec une vitesse moyenne de 0.004 secondes, avec un taux de 252 sudokus par seconde. Par contre, en choississant directement une case et valeur avec `random` (question 2), toutes les sudokus ont été résolus, avec une vitesse moyenne pareil à 0.0045 secondes mais un taux plus faible à 222 sudokus par seconde.

Tandis que la modification à l'algorithme dans (2) simplifie la recherche, ça n'aide pas avec la complexité vu que la recherche passe encore.

```
Question #1
Résous: 100/100 (100 Sudoku)
Temps: [moyenne:0.01 secondes, maximum: 0.02 secondes]

Question #2
Résous: 100/100 (100 Sudoku)
Temps: [moyenne: 0.01 secondes, maximum: 0.02 secondes]
```

Question 3
----------

Deux heuristiques supplémentaires ont été utilisées: celle de la variable la plus contraignante et celle de la valeur la moins contraignante.
Une source qui a été utilisée principalement est ["Solving Sudoku with AI"](https://towardsdatascience.com/solving-sudoku-with-ai-d6008993c7de), towardsDataScience.

L'heuristique de la variable la plus contraignante correspond à choisir la variable qui apparaît dans le plus de contraintes. Dans un problème de programmation sous contraintes standard cela a une utilité mais dans un sudoku chaque variable (case) a autant de contraintes (autant de pairs).
On peut donc modifier l'heuristique pour choisir la variable qui est "encore" la plus contraignante, soit celle qui a encore le plus de pairs non-fixés, afin de l'adapter au sudoku (standard).
On peut aussi modifier cet heuristique pour comptabiliser, au lieu du nombre de variables contraintes, le nombre de valeurs ^possibles de chaque variable qu'on contraindrait a, et essayer de maximiser cela (max).
On peut de même maximiser le nombre de valeurs possibles que chaque variable qu'on contraindrait a en commun avec la variable qu'on choisit et maximiser ceci (commun).

L'heuristique de la valeur la moins contraignante, elle, consiste à assigner la valeur la moins présente parmi les possibilités pour les pairs.

Chaque combinaison de version de la variable la plus contraignante et de la valeur la moins contraignante permet de créer une version avec des heuristiques différentes, qu'on peut comparer.

On a donc 6 versions à tester en plus de la version initiale.

Après plusieurs exécutions, les résultats semblent être les suivants:




On a donc que la combinaisons heuristique "binaire" et valeur la moins contraignante semble être la meilleure.

C'est donc celle-ci qui est implémentée dans le fichier sudoku3.py

Question 4
-----------
ficher :`sudoku4.py`

L'algorithme utilisé est le Hill-Climbing. Il est beaucoup moins efficace que Norvig, avec un taux de réussite de 44%. Il les fait résoudre à 50 sudokus par seconde ; une moyenne de 0.02 secondes pour chaque.

La complexité est: `O(infini)`,  car c'est un algorithme non optimal.
```
Question #4
Résous: 44/100 (100 Sudoku)
Temps: [moyenne: 0.02 secondes, maximum: 0.08 secondes]
```

Question 5
-----------
ficher :`sudoku5.py`

L'algorithme utilisé est le Simulated Annealing. 
Nous remarquons qu'il est plus lent en terme d'exécution
que le Hill-Climbing toutefois, il est plus optimal que ce dernier. D'autre part, en
comparaison avec l'implémentation en (1) et (2), il est relativement moins rapide. 

Par rapport aux performances, il résoud en moyenne seulement 5 sudokus 
par seconde, soit 0.17 secondes par sudoku, avec un maximum de 0.75 secondes. Cela,
varie beaucoup avec le temps `limit`. En effet, plus `limit` est petit, moins l'algorithme
est performant tout en ayant un temps d'exécution relativement faible.

La complexité est: `O(10kn^2)`,  avec la n la taille du Sudoku.
```
Question #5
Résous: 85/100
Temps: [moyenne: 0.17 secondes, maximum: 0.75 secondes]
```
