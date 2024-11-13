## 1/

*Que manque-t-il ? Et pourquoi ?*
	__Il manque un id qui permet de spécifier que chaque valeur est unique dans la liste qui, dans ce cas, est ‘\.self’__

## 2/

*Expliquez le changement que j’ai effectué par rapport à l’exemple précédent.*
*Pourquoi utiliser un ForEach ? Quel est son rôle ? Et pourquoi séparer le bouton du ForEach ?*
	__Ajout d’une fonction permettant d’ajouter dynamiquement un item. Ajout d’un bouton “Ajouter”.__
	__Le ForEach permet d’afficher chaque item présent dans loot et dans le cas actuel permettre de mettre à jour la vue. Séparer le bouton permet d’ajouter un item unique et non pas la liste complète.__

## 3/

*Testez ce code, fonctionne-t-il ? Pourquoi ?*
*Corrigez le code pour que le clique sur bouton “Ajouter” fonctionne, utilisez @State pour cela.*
*Expliquez pourquoi maintenant cela fonctionne ?*
	__Le code ne fonctionne pas car la liste est immutable.__
	__Ajouter @State permet de rendre la liste mutable (modifiable). Cela permet à la vue de lire et de modifier la valeur.__
