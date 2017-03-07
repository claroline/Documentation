### Configurer la connexion à Claroline Connect via Office 365
---


* Connectez-vous au [Microsoft account Developer Center](https://apps.dev.microsoft.com/#/appList) à l'aide de vos identifiants Office 365 et cliquez sur **Add an app**.

![](images/windows-add-app.png)

* Donnez un nom à votre application et cliquez sur **Create application**.

![](images/windows_new_app_create.jpg)

* Votre application est créée et vous êtes redirigé vers la page de configuration de votre app.

Vous y trouvez votre **Application ID** que vous allez copier-coller sur votre plateforme dans **Administration -> Paramètres de la plateforme -> Oauth -> Windows Live** dans l'espace réservé à l'**ID de l'application**.

![](images/windows-your-credentials.png)

* Cliquez sur **Generate New Password** pour obtenir un mot de passe.

![](images/o365-generate-password.png)

C'est ce mot de passe que vous allez copier-coller sur votre plateforme dans **Administration -> Paramètres de la plateforme -> Oauth -> Windows Live** dans l'espace réservé au **Secret de l'application**.

Attention: C'est la seule fois que ce mot de passe sera visible. Pensez à le sauvegarder dans un endroit sûr. En cas de perte, revenez ici pour en générer un nouveau.

![](images/o365-settings.png)

* Cliquez sur **Add Platform** dans la section **Platforms**.

![](images/windows-add-platform.png)

* Choisissez **Web**.

* Remplissez l'URL de redirection au format :
    
    http://VOTRE_NOM_DE_DOMAINE/login/check-o365

    Exemple: http://3l.claroline.com/login/check-o365

![](images/o365-url.png)

* Remplissez éventuellement les informations dans la section **Profile** et cliquez sur **Save**.
