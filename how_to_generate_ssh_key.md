## Générer une clé SSH pour GitHub

**1. Ouvrir un terminal**

* Sur Windows, recherchez "Invite de commandes" ou "Powershell".
* Sur Mac ou Linux, ouvrez un terminal.

**2. Générer la clé SSH**

Exécutez la commande suivante :

```
ssh-keygen -t ed25519 -C "votre_adresse_email@github.com"
```

Remplacez `votre_adresse_email@github.com` par votre adresse email GitHub.

**3. Choisir l'emplacement de la clé**

Appuyez sur Entrée pour accepter l'emplacement par défaut ou entrez un nom de fichier personnalisé.

**4. Définir une phrase de passe (facultatif)**

Appuyez sur Entrée pour ignorer la phrase de passe ou entrez une phrase de passe si vous souhaitez une sécurité accrue.

**5. Copier la clé publique**

Exécutez la commande suivante pour afficher votre clé publique :

```
cat ~/.ssh/id_ed25519.pub
```

Sélectionnez et copiez la clé entière, y compris la ligne commençant par `ssh-ed25519`.

**6. Ajouter la clé SSH à GitHub**

* Accédez à votre compte GitHub et ouvrez **Paramètres** > **SSH et clés GPG**.
* Cliquez sur **Nouveau** > **Ajouter une clé SSH**.
* Collez votre clé publique dans le champ **Clé SSH**.
* Cliquez sur **Ajouter une clé SSH**.

**7. Tester la connexion SSH**

Exécutez la commande suivante pour tester votre connexion à GitHub :

```
ssh -T git@github.com
```

Si vous êtes connecté avec succès, vous verrez un message indiquant "Hi your_username!".

**Ressources supplémentaires:**

* Documentation GitHub: [https://docs.github.com/fr/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent](https://docs.github.com/fr/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
