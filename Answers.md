# App Basic
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

# Ajout Items
## 1/

*Tester ce code, il devrait compiler.
Cliquez sur le bouton “Ajouter” (de la liste), que se passe-t-il ? Pourquoi cela ne marche pas ?
*
	__Une erreur s'affiche dans la console.
 	N'ayant pas de lien entre la class et la struct, aucune mise a jour ne peut s'appliquer entre la méthode et l'affichage (aucune mise a jour de l'état de l'inventaire)__

## 2/

*Utiliser @StateObject, ObservableObject et @Published pour que l’ajout d’un item fonctionne.
Pourquoi cela fonctionne de nouveau ?
Pourquoi utiliser @StateObject plutôt que @ObservedObject ou @State ?
*
 	__"ObservableObject est utilisé pour créer des objets dont les propriétés publiées déclenchent automatiquement des mises à jour de l’interface utilisateur lorsqu’elles changent."
  	"@Published est utilisé pour déclarer des propriétés d’un objet observable dont la modification entraîne une mise à jour de l’interface utilisateur."
   	"StateObject est utilisé pour initialiser un objet observable en tant que propriété d’une vue et garantit que l’objet est créé une seule fois."
	Tout cela permet de rendre l'objet observable et donc modifiable.
 	StateObject permet d'initialiser une unique fois l'objet et le rendre modifiable.__
