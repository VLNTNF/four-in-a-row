# Une IA pour jouer au puissance 4

## Explication
Notre méthode de recherche est un alpha-beta (*alpha-beta-searching(s)*).  

Notre heuristique est dans *Utility(s)*. Cette méthode parcourt toute la grille. Pour chaque case, elle regarde selon la colonne, la ligne et les deux diagonales si des jetons sont alignés. Elle additionne alors si : 
-	2 jetons sont alignés pour l’IA : +10
-	3 jetons sont alignés pour l’IA : +100
-	4 jetons sont alignés pour l’IA : +10000

-	2 jetons sont alignés pour l’adversaire : -10
-	3 jetons sont alignés pour l’adversaire : -100
-	4 jetons sont alignés pour l’adversaire : -10000

Pour tester si la partie est terminée, *TerminalTest(s)* regarde en parcourant toute la grille si 4 jetons sont alignés ou si la ligne du haut, soit *s[0]*, est rempli de chiffre « non-zero ».  

Pour déterminer les actions possibles, la méthode *Actions(s)* détermine dans la ligne du haut *s[0]* les positions où la valeur est nulle.  

Pour éviter de modifier la grille en cherchant la bonne solution, il a une distinction entre *Result(s, a, p)* et *ResultTest(s, a, p)*. Cette dernière fait une copie de la grille en utilisant la librairie *copy*.  

Les méthodes *QuiCommence()* et *Demande()* permettent de faire fonctionner le jeu en demandant qui commence et les actions de l’adversaire. 

Enfin la librairie *timeit* a été importée pour mesurer le temps de décision de l’IA dans la méthode *Jeu()*. 

## Jouer maintenant
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VLNTNF/four-in-a-row-bot/blob/main/Puissance4.ipynb)
