---
name: BugFix Flag
about: Le personnage player n'est pas stoppé par les obstacles
title: "[BugFix][Pico8][Flag] Impossible de générer des obstacles"
labels: enhancement
assignees: ''

---
Description :
- assignation d'un flag au sprite correspondant à un obstacle
- utilisation de la fonction check_flag()
Et pourtant le mouvement du personnage n'est pas stoppé quand il arrive sur un sprite "flaggé" en obstacle.

Résolution :
Le flag se rapporte à un sprite qui correspond lui-même à une tile. Il est donc nécessaire que le personnage se déplace par tile, et non par pixel. Dans la fonction draw_player(), il faut donc ajouter x8 (asterisque 8) aux coordonnées du sprite.


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
