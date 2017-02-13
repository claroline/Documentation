### Enregistrer et configurer une App Facebook
---

<p style="color: red">Ajouter les captures d'écran !!!</p>

Commencez par vous connecter à Facebook

Allez à Facebook Developers Apps. Vous avez besoin d'un compte Facebook Développeur pour démarrer. Si vous n'en avez pas, mettez votre compte Facebook personnel à jour vers un compte Facebook Développeur.

Cliquez sur le bouton **+Add a New Ap** ou utilisez le menu déroulant **My Apps** et choisissez **Add a New App**.

![](/fr/admin/images/fb_new_app_new_button.jpg)

![](/fr/admin/images/fb_new_app_menu.jpg)

Choisissez **Basic setup** lorsqu'on vous demande de choisir une plateforme.

![](/fr/admin/oauth/images/fb_new_app_choice.jpg)

Donnez un nom à votre App dans le champ "Display Name", choisissez **Apps for Pages** comme **Catégorie** et cliquez pour **Create a New App ID**.

![](/fr/admin/oauth/images/fb_new_app_properties.jpg)

Complétez le **Security Check**.

Votre App est créée à présent! Copiez l'ID de l'App et le Secret de l'App du tableau de bord et copiez-les dans Claroline: Administration -> Paramètres de la platforme -> Oauth -> Facebook. Remplissez les champs **ID de l'application" et "Secret de l'application".

Configurez à présent votre App. Allez dans les **Paramètres", donnez un courriel valide dans l'onglet "Basic" et cliquez sur "Save".

Allez dans l'onglet **Advanced** et sélectionnez **Client OAuth Settings**. Choisissez l'option **Embedded Browser OAuth Login** et pour le **Valid OAuth redirect URL**, écrivez votre URL sous la forme suivante: _http://YOUR_DOMAIN_NAME/login/check-facebook_

_Exemple: http://3l.claroline.com/login/check-facebook_

![](/fr/admin/oauth/images/fb_app_enable_browser_add_redirect.jpg)

Allez sur **App Review** et à la question _"Do you want to make this app and all its live features available to the general public?"_, répondez **Yes* de façon à publier votre App.

Félicitations! Vous avez configuré votre App Facebook!