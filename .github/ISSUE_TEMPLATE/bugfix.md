---
name: BugFix Disparition d'un personnage statique
about: Quand les 2 personnages se rencontrent, le personnage statique, secondaire, ne disparait pas
title: "[BugFix][Pico8][Pick_up][Interact] Impossible d'enchaîner une réponse à une interaction"
labels: enhancement
assignees: ''

---
Description :
- le personnage player cherche un personnage secondaire statique
- quand il le trouve, le sprite du personnage player passe derrière et seul reste le sprite du personnage secondaire

Résolution :
Elle se fait grâce à une modification de statut. 

Puisque le personnage est statique, il vaut mieux considérer le personnage secondaire comme un objet, plutôt que comme un personnage. Le sprite doit donc être intégrer à la map, et non par le biais des fonctions create_p() et draw_p().

Dans la fenêtre de création des sprites :
- nécessaire d'assigner un flag à ce sprite, 
- de le faire suivre par un sprite sans flag, qui reprendra le visuel sans l'objet/ personnage, pour utiliser la fonction next_tile().


---
name: BugFix
about: Décrivez un bug et ses moyens de résolution
title: "[BugFix]"
labels: enhancement
assignees: ''

---

**Donnez un titre à votre Bug Fix**
Ajoutez entre crochets les tags pertinents parmi :
[BugFix][Device][OS][Logiciel][Version] Titre
Par exemple : "[BugFix][iOS][Safari] Impossible de se connecter au compte utilisateur"

**Décrivez-la**
Dans quel contexte le bug s'est-il produit ? Il est important de donner le plus d'informations
possibles : machine, logiciel, version, URL.
Le bug est-il reproductible : les devs sont-ils capables de recréer les conditions d'apparition
du bug ?
Si vous possédez une capture d'écran, vous pouvez la joindre.

**Résolution du bug**
Quelles sont les étapes pour résoudre ce bug ? Il est important de tester sa résolution
dans les mêmes conditions que celles d'apparition.
Vous pouvez ajouter une checklist comme pour une feature classique.
