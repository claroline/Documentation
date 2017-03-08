### Enregistrer et configurer une App Windows Live
---

**Attention: Si vous désirez utiliser la connexion via Windows Live, il faut que votre serveur web soit configuré en https. Vous devrez aussi activer le SSL dans les paramètres de votre plateforme.**

* Connectez-vous au [Microsoft account Developer Center](https://apps.dev.microsoft.com/#/appList) à l'aide de vos identifiants Windows et cliquez sur **Add an app**.

![](images/windows-add-app.png)

* Donnez un nom à votre application et cliquez sur **Create application**.

![](images/windows_new_app_create.jpg)

* Votre application est créée et vous êtes redirigé vers la page de configuration de votre app.

Vous y trouvez votre **Application ID**.

![](images/windows-your-credentials.png)

* Cliquez sur **Generate New Password** pour obtenir un mot de passe correspondant au secret à copier-coller sur votre plateforme dans **Administration -> Paramètres de la plateforme -> Oauth -> Windows Live**.

![](/fr/admin/oauth/images/windows-app-secret.png)

* Cliquez sur **Add Pplatform** dans la section **Platforms**.

![](images/windows-add-platform.png)

* Choisissez **Web**.

![](images/windows-add-web.png)

![](images/windows-your-credentials.png)

* Remplissez l'URL de redirection au format :
    
    https://VOTRE_NOM_DE_DOMAINE/login/check-windows

    Exemple: https://3l.claroline.com/login/check-windows

![](/fr/admin/oauth/images/windows-https.png)

* Remplissez éventuellement les informations dans la section **Profile** et cliquez sur **Save**.
