# Evaluation Conception d'une solution en temps réel

## Diagramme :

J'ai rapidement réalisé un diagramme :

https://docs.google.com/spreadsheets/d/16qTEYlryOO9Wl31pkanRVSAFVOe1gkPh5-BAu7p8mkQ/edit

Ce digramme est loins d'etre parfait mais il permet de modéliser rapidement l'exécution et nous permet de voir que la période de chaque
tache est très faible. 

De plus j'ai calculé le taux de charges du processeur : 

U = 2/5 + 3/15 + 5/5 + 3/5 
U = 2/5 + 1/5 + 5/5 + 3/5
U = 11/5 = 2.2 

Donc U > 1, le contraintes de temps ne peuvent donc pas etre respecter. Cela n'est pas très grave car toutes les taches sont
du soft real time. Mais il est important de le noter malgré tout. 

## Algorythme

Pour écrire notre algorythme, nous allons supposé plusieurs choses :
- L'appel des pompes doit etre alterné
- Si une machine peut etre utilisé (c'est à dire que la quantité d'huile est suffisante) alors elle prends la priorité sur les pompes.

## Programme Python

Le programme est le Scheduler.py.
Sur la branche main, vous retrouverez le Scheduler sans prendre en compte la période. 
Sur la branche periode, vous retrouvez le Scheduler en prenant en compte la période. 

## Résultat 

Vous pouvez trouvez les résultats et tout les log dans result.txt 
