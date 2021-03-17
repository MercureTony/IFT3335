Rapport TP1 – IFT3335
=====================

Étienne Beaulé (20120318), Nicolas Soriano, Anthony Uyende (20117140)

Le code pour chaque question est dans le fichier `sudokuN.py`, `N` étant le numéro de la question. C'est en Python3.

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
Question 4
-----------
L'algorithme utilisé est le Hill-Climbing. Il est beaucoup moins efficace que Norvig, avec un taux de réussite de 44%. Il les fait résoudre à 50 sudokus par seconde ; une moyenne de 0.02 secondes pour chaque.

La complexité est: `O(infini)`,  car c'est un algorithme non optimal.
```
Question #4
Résous: 44/100 (100 Sudoku)
Temps: [moyenne: 0.02 secondes, maximum: 0.08 secondes]
```

Question 5
-----------
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
