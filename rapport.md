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
L'algorithme utilisé est le Hill-Climbing
```
Question #5


(100 Sudoku)
Résous: 100/100
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]

(1000 Sudoku)
Résous: 100/100
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]

(95 Sudoku)
Résous: 95/95
Temps: [moyenne: 0.01 secondes, maximum: 0.07 secondes]
```

Question 5
-----------
L'algorithme utilisé est le Simulated Annealing
```
Question #5
(100 Sudoku)
Résous: 100/100
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]

(1000 Sudoku)
Résous: 100/100
Temps: [moyenne: 0.00 secondes, maximum: 0.02 secondes]

(95 Sudoku)
Résous: 95/95
Temps: [moyenne: 0.02 secondes, maximum: 0.09 secondes]
```
