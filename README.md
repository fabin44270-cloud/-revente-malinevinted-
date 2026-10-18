# Revente Maline — APK Android avec relais des notifications Vinted

Cette version reprend l'application Revente Maline (calcul de marge, stock, historique) et ajoute un relais des notifications Vinted vers une notification Android Revente Maline.

## Limite importante — ce n'est PAS un robot qui scrape Vinted

- L'application ne se connecte pas au compte Vinted et ne parcourt pas toutes les annonces en arrière-plan.
- Elle ne contourne pas les protections anti-robots et ne garantit pas que Vinted envoie une alerte pour chaque nouvelle annonce.
- Elle relaie les notifications émises par l'application Vinted si Android lui accorde l'accès aux notifications. Elle ne copie ni n'enregistre le contenu des messages Vinted ; la notification relayée est générique.
- Pour recevoir des alertes de bonnes affaires, configure d'abord dans Vinted les recherches enregistrées/notifications proposées par Vinted. La disponibilité de ces alertes varie selon les fonctions et paramètres de Vinted.
- La fonction nécessite que l'application Vinted soit installée et que les notifications Vinted soient activées. Les économies de batterie Android peuvent retarder les notifications.

## Créer l'APK depuis un téléphone Android (sans Android Studio)

1. Télécharge ce ZIP et décompresse-le dans l'application Fichiers de ton téléphone.
2. Dans Chrome, ouvre https://github.com et connecte-toi (ou crée un compte).
3. Appuie sur **+** puis **New repository**. Nom : `revente-maline`. Choisis **Public**, puis crée le dépôt.
4. Dans le dépôt, appuie sur **Add file** puis **Upload files**.
5. Ouvre le dossier décompressé et sélectionne TOUS les fichiers et dossiers à l'intérieur de `revente_maline_apk`, y compris le dossier caché `.github`. Si le sélecteur Android ne montre pas les fichiers cachés, active l'affichage des fichiers cachés ou utilise l'option GitHub web d'envoi de fichiers. Les fichiers doivent se trouver à la racine du dépôt : `app`, `.github`, `build.gradle`, `settings.gradle`, etc. PAS dans un sous-dossier supplémentaire.
6. Valide avec **Commit changes**.
7. Dans GitHub, ouvre **Actions**. Sélectionne **Build Revente Maline APK** puis **Run workflow** si le build n'a pas démarré automatiquement.
8. Attends la coche verte. Ouvre l'exécution terminée, descends jusqu'à **Artifacts**, puis télécharge `revente-maline-apk`.
9. Décompresse l'archive de l'artefact : elle contient `app-debug.apk`. Ouvre ce fichier sur Android pour l'installer. Autorise l'installation depuis cette source si Android le demande.
10. Ouvre Revente Maline, puis **Surveillance Vinted** > **Activer l'accès aux notifications**. Dans les réglages Android, active **Alertes Vinted – Revente Maline**.
11. Dans Vinted, active les notifications et configure les alertes de recherches que l'application Vinted propose. Fais un essai avec une notification Vinted.

## Dépannage

- Si GitHub ne montre pas le dossier `.github`, le workflow de compilation risque de ne pas être envoyé : active l'affichage des fichiers cachés dans le gestionnaire de fichiers ou importe le ZIP depuis un ordinateur.
- Si l'APK ne se compile pas, ouvre l'exécution rouge dans Actions et copie le premier message d'erreur pour le dépannage.
- L'APK produite est une APK de test (`app-debug.apk`), pas une version publiée sur Play Store.
- Les données de stock sont locales à l'application. Fais une sauvegarde depuis les fonctions de l'application.
