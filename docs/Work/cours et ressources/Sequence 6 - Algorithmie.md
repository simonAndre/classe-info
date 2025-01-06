---
share: true
---

[back - Séquences](../../../S%C3%A9quences.md#)






## Activité débranchée : Le problème du tri en 2 piles:
activité intéressante pour découvrir la notion d’algorithme et l'intérêt d'exprimer de manière claire une méthode de résolution.

Soit une pile de livres, comment la trier en n'utilisant que 2 piles : les livres ne peuvent être posés ailleurs que sur l'une des 2 piles. Vous Tenterez de trouver la méthode de résolution puis vous l'écrirez de façon à ce qu' un autre groupe puisse l'appliquer uniquement en lisant vos instructions. 

- tant qu'il y a des livres sur la pile A:
	- trouver le plus petit de la pile A => pos_a
	- prendre tous les livres au dessus du plus petit (inclus), les déposer sur la pile B => pos_b
	- prendre les livres au dessus pos_b (non inclus), les déposer au sommet de pile A
	- boucler
retrouver aussi les pb de tri du crépier psychorigide.

## notions
- invariant de boucle : Une propriété qui reste vraie pendant toute l'execution du programme et notamment : au démarrage (avant le premier tour de boucle) et à la fin du programme lorsque l'on sort de la boucle.
## présentation d'autres algorithmes de tri à connaitre
#### tri par selection : 
0<--partie gauche-->i<--partie droite-->n
invariants:
	- la partie gauche est triée
	- la partie droite n'est pas triée, tous les éléments de la partie droite sont > aux éléments de la partie gauche
Algo:
- tant que partie droite non vide:
	- on prend le plus petit de la partie droite, 
	- on l'échange avec e[i-1]
	- on avance i de 1

#### tri par insertion : 
0<--partie gauche-->i<--partie droite-->n
invariants:
	- la partie gauche est triée
	- la partie droite n'est pas triée,
Algo:
- tant que partie droite non vide:
	- on prend l'élément i, on l'échange avec les élément situés à sa gauche tant que ces éléments sont plus grands que lui
	- on avance i de 1
3 6 7 1 8 2 5 9 4
i=1

| i   | t[i] | t (e fin d'itération) |
| --- | ---- | --------------------- |
| 1   | 6    | 3 6 7 1 8 2 5 9 4     |
| 2   | 7    | 3 6 7 1 8 2 5 9 4     |
| 3   | 1    | 1 3 6 7 8 2 5 9 4     |
| 4   | 8    | 1 3 6 7 8 2 5 9 4     |
| 5   | 2    | 1 2 3 6 7 8 5 9 4     |
| 6   | 5    | 1 2 3 5 6 7 8 9 4     |
| 7   | 9    | 1 2 3 5 6 7 8 9 4     |
| 8   | 4    | 1 2 3 4 5 6 7 8 9     |
