Rapport TP1 – IFT3335
=====================

Étienne Beaulé (20120318), Nicolas Soriano, Anthony Uyende (20117140)

Questions 1 & 2
---------------

Le code fourni fonctionnait bien à part le chronomètre pour les tests qui était désuet et enlèvé à la version 3.3 de Python. On l'a donc remplacé. On a aussi remplacé le fichier de tests pour `100sudoku.txt`.

Sans modification substantielle (la question 1), tous les sudokus ont été réussis avec une vitesse moyenne de 0.004 secondes, avec un taux de 252 sudokus par seconde. Par contre, en choississant directement une case et valeur avec `random` (question 2), seulement 54 des 100 sudokus ont été résolus, avec une vitesse moyenne un peu plus bas à 0.003 secondes et un taux de 288 sudokus par seconde.

Tandis que la modification à l'algorithme dans (2) simplifie la recherche, ça n'aide pas avec la complexité vu que la recherche passe encore, mais avec moins de réussite.

```
Question #1
Résous: 100/100 (100 Sudoku)
Temps: [moyenne:0.01 secondes, maximum: 0.02 secondes]

Question #2
Résous: 51/100 (100 Sudoku)
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]
```
Question 4
-----------
L'algorithme utilisé est le Hill-Climbing

(100 Sudoku)
```
Résous: 100/100
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]
```
(1000 Sudoku)
```
Résous: 1000/1000
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]
```
(95 Sudoku)
```
Résous: 95/95
Temps: [moyenne: 0.01 secondes, maximum: 0.07 secondes]
```

Question 5
-----------
L'algorithme utilisé est le Simulated Annealing

(100 Sudoku)
```
Résous: 100/100
Temps: [moyenne: 0.00 secondes, maximum: 0.01 secondes]
```
(1000 Sudoku)
```
Résous: 1000/1000
Temps: [moyenne: 0.00 secondes, maximum: 0.02 secondes]
```
(95 Sudoku)
```
Résous: 95/95
Temps: [moyenne: 0.02 secondes, maximum: 0.09 secondes]
```