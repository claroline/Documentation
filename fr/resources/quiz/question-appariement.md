### Question Appariement

---

La question appariement permet de créer des questions où les utilisateurs devront mettre par paire des éléments. Ces éléments peuvent être du texte, une image, du son ou une vidéo. En d'autres termes, l'utilisateur aura un ensemble d'items \(colonne de gauche\) qu'il faudra remettre par paire \(colonne de droite\).

Lorsque vous avez rempli les champs communs à toutes les questions \(cf. [Créer une nouvelle question](create_new_question.md) \), vous devez remplir le formulaire spécifique à la question appariement.

#### Pénalité pour toute mauvaise réponse non définie

Vous pouvez définir dans ce champ une pénalité pour toute erreur effectuée par l'utilisateur lors de la passation. Cette pénalité exprimée en points positifs, par exemple 1 point de pénalité équivaudra a un retrait de 1 point du score total de la question pour chaque réponse erronée. Cela peut donc engendrer des scores négatifs.

Cette pénalité ne se cumule pas à des réponses erronées que le concepteur aurait déjà défini \(paire avec un score négatif\).

#### **Ordre des paires aléatoires**

En cochant cette option, vos paires \(éléments de la droite\) seront disposées aléatoirement lors de la passation. Attention, on parle ici des paires et non des items à mettre par paire \(éléments de la gauche\) qui seront eux toujours disposés aléatoirement. A contrario, si vous ne la cochez pas, les paires seront affichées dans l'ordre dans lesquels vous les aurez créés.

Cette option n'a de sens que si certains items sont déjà pré-positionnés \(item épinglé\).

#### Créer les paires

Le remplissage du formulaire s'organise en deux temps : vous devez créer vos items puis les déplacer pour créer les paires que vous souhaitez.

* **Création des items **

Les items peuvent être du texte simple, une image, une vidéo ou encore un audio \(en utilisant l'éditeur de texte riche\).  Vous créez des items dans la colonne de gauche tel

Si vous souhaitez rajouter de la complexité, vous pouvez ajouter un intrus en cliquant sur "ajouter un intrus". Cet intrus est associé à un score \(nul ou négatif\) et peut aussi avoir un feedback. 

Le feedback est un message non obligatoire que vous pouvez adresser à l'utilisateur si celui-ci apparie l'intrus à un autre item au moment de la passation. Ce feedback sera affiché en fin d'étape si cette option a été choisie dans les paramètres du questionnaire \(cf. "Afficher les feedbacks en fin d'étape" dans  [Correction](quiz_parameters_correction.md)\) ainsi que dans la correction.  
En cliquant sur l'icône  : ![](images/quiz-fig20.png), vous ouvrez le champ texte où vous écrirez le feedback.

Ce score sera comptabilisé seulement si l'utilisateur a apparié cet intrus. Il en est de même pour l'affichage du feedback.

La poubelle vous permet de supprimer l'intrus.

* **Création des paires**

Une fois les items créés, vous pouvez former les paires. 

Pour cela vous devez déplacer un item dans chacune des zones prévue à cet effet \(2 par paire\). Chaque paire est associé à un score et un feedback \(facultatif\). Vous pouvez lui associer un score positif, nul ou négatif.

Cliquez sur "ajouter une paire" pour ajouter d'autres paires.

Vous pouvez choisir d'épingler un item pour qu'il soit visible lors de la passation. Ainsi l'utilisateur n'aura qu'un item à déplacer pour compléter la paire. Vous devez pour cela cocher "Activer / désactiver la fonctionnalité épingler un item" puis choisir l'item que vous allez épingler.

Voici un exemple de conception d'une question.

