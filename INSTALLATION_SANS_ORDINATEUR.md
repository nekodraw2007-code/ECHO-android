# Installer ECHO sur une tablette sans ordinateur

Ce projet peut être compilé sur les serveurs gratuits de GitHub Actions. La tablette ne fait que téléverser les fichiers et télécharger l'APK.

## Étapes
1. Crée un compte sur https://github.com si tu n'en as pas.
2. Dans Chrome sur la tablette, ouvre https://github.com/new et crée un dépôt nommé `ECHO-Android`. Choisis **Public** (nécessaire pour utiliser les minutes gratuites plus simplement), puis **Create repository**.
3. Dans le dépôt, touche **Add file > Upload files**.
4. Décompresse l'archive ZIP sur la tablette avec son gestionnaire de fichiers.
5. Téléverse le CONTENU du dossier `ECHO` (pas le dossier parent lui-même), y compris le dossier caché `.github` et son fichier `workflows/build-apk.yml`. Si le sélecteur Android ne permet pas d'ajouter les dossiers/fichiers cachés, cette méthode web peut être bloquée sur ton appareil.
6. Valide avec **Commit changes**.
7. Ouvre l'onglet **Actions** du dépôt, sélectionne **Construire ECHO APK**, puis **Run workflow** si le lancement automatique n'a pas déjà démarré.
8. Attends que le travail passe au vert. Ouvre son exécution, descends à **Artifacts**, puis télécharge `ECHO-APK`.
9. Décompresse l'archive d'artifact téléchargée : elle contient `app-debug.apk`.
10. Ouvre `app-debug.apk` sur la tablette et autorise l'installation depuis cette source si Android le demande.

## Important
- Cette compilation distante fabrique un APK à partir du code fourni ; elle ne remplace pas un test sur ta tablette.
- L'APK debug n'est pas publié sur le Play Store.
- Ne partage pas publiquement d'enregistrements audio ou vidéo privés dans le dépôt. Les données de session restent sur l'appareil si l'application les stocke localement.
