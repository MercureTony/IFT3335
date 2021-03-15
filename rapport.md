Rapport TP1 – IFT3335
=====================

Étienne Beaulé (20120318), Nicolas Soriano, Anthony Uyende

Questions 1 & 2
---------------

Le code fourni fonctionnait bien à part le chronomètre pour les tests qui était désuet et enlèvé à la version 3.3 de Python. On l'a donc remplacé. On a aussi remplacé le fichier de tests pour `100sudoku.txt`.

Sans modification substantielle (la question 1), tous les sudokus ont été réussis avec une vitesse moyenne de 0.004 secondes, avec un taux de 252 sudokus par seconde. Par contre, en choississant directement une case et valeur avec `random` (question 2), seulement 54 des 100 sudokus ont été résolus, avec une vitesse moyenne un peu plus bas à 0.003 secondes et un taux de 288 sudokus par seconde.

Tandis que la modification à l'algorithme dans (2) simplifie la recherche, ça n'aide pas avec la complexité vu que la recherche passe encore, mais avec moins de réussite.
