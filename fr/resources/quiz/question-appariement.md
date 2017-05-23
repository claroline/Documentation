### Question Appariement

---

La question appariement permet de créer des questions où les utilisateurs devront mettre  par paire des éléments. Ces éléments peuvent être du texte, une image, du son ou une vidéo. En d'autres termes, l'utilisateur aura un ensemble d'items \(colonne de gauche\) qu'il faudra remettre par paire \(colonne de droite\).

Lorsque vous avez remplis les champs communs à toutes les questions \(cf. [Créer une nouvelle question](create_new_question.md) \), vous devez remplir le formulaire spécifique à la question appariement.

#### Pénalité pour toute mauvaise réponse non définie

Vous pouvez définir dans ce champ une pénalité pour toute erreur effectuée par l'utilisateur lors de la passation. Cette pénalité exprimée en points positifs, par exemple 1 point de pénalité équivaudra a un retrait de 1 point du score total de la question pour chaque réponse erronée. Cela peut donc engendrer des scores négatifs.

Cette pénalité ne se cumule pas à des réponses erronées que le concepteur aurait déjà défini \(paire avec un score négatif\).

#### **Ordre des paires aléatoires**

En cochant cette option, vos paires \(éléments de la droite\) seront disposées aléatoirement lors de la passation. Attention, on parle ici des paires et non des items à mettre par paire \(éléments de la gauche\) qui seront eux toujours disposés aléatoirement. A contrario, si vous ne la cochez pas, les paires seront affichées dans l'ordre dans lesquels vous les aurez créés.

Cette option n'a de sens que si certains items sont déjà pré-positionnés \(item épinglé\). 

#### Créer les paires

Le remplissage du formulaire s'organise en deux temps : vous devez créer vos items, puis vous devrez les déplacer pour créer les paires que vous souhaitez.

* **Création des items **

Les items peuvent être du texte simple, une image, une vidéo ou encore un audio \(en utilisant l'éditeur de texte riche\).

Les items se répartissent en 2 colonnes : les items de la colonne de gauche devront être reliés à un ou plusieurs items de celle de droite. Vous devez donc remplir les items et les relier entre eux. en fonction des réponses attendues \(ou des erreurs attendues\). Pour cela, cliquez sur la pastille qui se trouve à droite d'un item de la colonne de gauche, maintenez le clic et déplacez la pastille jusqu'à la pastille qui se trouve à gauche de l'item de la colonne de droite auquel vous voulez l'associer. Quand vous relâchez le clic, un lien entre les 2 items se forme et une popover s'ouvre afin d'éditer l'association. Vous pourrez alors donner un score \(positif ou négatif\) et un feedback à l'association. La couleur de la liaison permet de voir si le score associé à la réponse est positif \(vert\) ou négatif ou nul \(rouge\).

Le feedback est un message non obligatoire que vous pouvez adresser à l'utilisateur si celui-ci crée cette liaison au moment de la passation. Ce feedback sera affiché en fin d'étape si cette option a été choisie dans les paramètres du questionnaire \(cf. "Afficher les feedbacks en fin d'étape" dans  [Correction](quiz_parameters_correction.md)\) ainsi que dans la correction.  
En cliquant sur l'icône  : ![](images/quiz-fig20.png), vous ouvrez le champ texte où vous écrirez le feedback.

Enfin, la poubelle vous permet de supprimer la liaison.

Pour fermer cette popover d'édition de l'association cliquez sur la croix en haut à droite.

Si vous souhaitez qu'il y ait des intrus, il vous suffit de ne pas associer un item avec un autre.

* **Création des paires**

#### Activer / désactiver la fonctionnalité épingler un item

Voici un exemple de conception d'une question.



