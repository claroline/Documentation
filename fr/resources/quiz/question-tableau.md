### Question Tableau

---

La question tableau permet de créer des questions où les utilisateurs devra combler des lacunes dans un tableau. Il est possible de les compléter soit en rédigeant une zone texte soit en choisissant l'élément dans une liste prédéfinie.


Lorsque vous avez rempli les champs communs à toutes les questions \(cf. [Créer une nouvelle question](create_new_question.md) \), vous devez remplir le formulaire spécifique à la question tableau.

![](images/quiz-fig54.png)

#### Type de score

Pour la question tableau, le score peut être comptabilisé de manières différentes

- **Score par cellule** : chaque cellule possède un score. C'est le mode par défaut.
- **Score par colonne** : chaque colonne possède un score. Les points seront attribués seulement si toute la colonne est juste.
- **Score par ligne** : chaque ligne possède un score. Les points seront attribués seulement si toute la ligne est juste.
- **Score global** : les points seront attribués seulement si tout est juste \(points en cas de succès\). S'il y a ne serait-ce qu'une erreur, ce seront les points en cas d'échec qui seront attribués \(ils peuvent être nuls ou négatifs\).



#### Pénalité pour toute mauvaise réponse non définie

Vous pouvez définir dans ce champ une pénalité pour toute erreur effectuée par l'utilisateur lors de la passation. Cette pénalité exprimée en points positifs, par exemple 1 point de pénalité équivaudra a un retrait de 1 point du score total de la question pour chaque réponse erronée. Cela peut donc engendrer des scores négatifs.

Cette pénalité ne se cumule pas à des réponses erronées que le concepteur aurait déjà défini \(association avec un score négatif\).


#### Paramétrer le tableau

- **Taille** : c'est dans ces champs que vous devez définir le nombre de lignes et de colonnes que votre tableau aura.
- **Bordure** : Vous pouvez définir l'épaisseur de la bordure de votre tableau en entrant une valeur numérique. La couleur de la bordure peut être définie en cliquant sur le pinceau.

#### Remplir le tableau

Une fois votre tableau généré, vous devez le remplir tel un texte à trous. 
Tout d'abord remplissez les cellules avec le texte que vous souhaitez. Vous pouvez modifier la couleur de la cellule ainsi que la couleur de la police en cliquant sur les icônes en haut à gauche de la cellule.

Pour créer une cellule qui devra être rempli par l'utilisateur lors de la passation, cliquez sur le "+" en haut à droite de la cellule. En cliquant dessus, une popover s'ouvre afin d'éditer le trou. 

Vous pourrez alors donner un score \(positif ou négatif\) et un feedback au mot que l'utilisateur devra taper. La couleur de la liaison permet de voir si le score associé à la réponse est positif \(vert\) ou négatif ou nul \(rouge\).

Vous pouvez donner plusieurs propositions de réponses voire anticiper les mauvaises.

En cochant l'option "soumettre une liste", l'utilisateur aura une liste déroulante lors de la passation et devra choisir entre différentes propositions (via un menu déroulant).  Pour utiliser cette option il faut donc que la cellule ait au moins une réponse correcte (score positif) et plusieurs propositions erronées (score nul ou négatif).

Le feedback est un message non obligatoire que vous pouvez adresser à l'utilisateur si celui-ci crée cette liaison au moment de la passation. Ce feedback sera affiché en fin d'étape si cette option a été choisie dans les paramètres du questionnaire \(cf. "Afficher les feedbacks en fin d'étape" dans  [Correction](quiz_parameters_correction.md)\) ainsi que dans la correction.  
En cliquant sur l'icône  : ![](images/quiz-fig20.png), vous ouvrez le champ texte où vous écrirez le feedback.

Enfin, la poubelle vous permet de supprimer la liaison.

Pour fermer cette popover d'édition de l'association cliquez sur la croix en haut à droite.





