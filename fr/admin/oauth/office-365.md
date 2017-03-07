### Enregistrer et configurer une App Office 365
---


* Connectez-vous au [Microsoft account Developer Center](https://apps.dev.microsoft.com/#/appList) à l'aide de vos identifiants Windows et cliquez sur **Add an app**.

![](images/windows-add-app.png)

* Donnez un nom à votre application et cliquez sur **Create application**.

![](images/windows_new_app_create.jpg)

* Votre application est créée et vous êtes redirigé vers la page de configuration de votre app.

Vous y trouvez votre **Application ID**.

![](images/windows-your-credentials.png)

* Cliquez sur **Generate New Password** pour obtenir un mot de passe correspondant au secret à copier-coller sur votre plateforme dans **Administration -> Paramètres de la plateforme -> Oauth -> Windows Live**.

* Cliquez sur **Add Pplatform** dans la section **Platforms**.

![](images/windows-add-platform.png)

* Choisissez **Web**.

![](images/windows-add-web.png)

![](images/o365-your-credentials.png)

* Remplissez l'URL de redirection au format :
    
    http://VOTRE_NOM_DE_DOMAINE/login/check-o365

    Exemple: http://3l.claroline.com/login/check-o365

![](/fr/admin/oauth/images/o365-url.png)

* Remplissez éventuellement les informations dans la section **Profile** et cliquez sur **Save**.
