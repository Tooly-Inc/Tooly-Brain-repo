# 🔊 Zoho Creator Audio Scan Widget

Ce widget permet d'ajouter un retour sonore (succès/erreur) lors d'une saisie ou d'un scan de code-barres dans **Zoho Creator**. Il utilise l'API native du navigateur pour générer les sons sans dépendances externes.

## 🚀 Fonctionnalités
* **Validation Sonore :** Bip aigu pour un succès, buzz grave pour une erreur.
* **Compatibilité Douchette :** Déclenchement automatique via la touche "Entrée" simulée par les lecteurs de codes-barres.
* **Auto-Focus :** Le curseur revient automatiquement dans le champ après chaque scan pour une saisie en continu.
* **Léger & Gratuit :** Aucun fichier audio (`.mp3`) à héberger, utilise la **Web Audio API**.

## 🛠️ Installation dans Zoho Creator

1.  **Préparation :** Enregistrez le code HTML dans un fichier nommé `index.html`.
2.  **Compression :** Mettez ce fichier dans un dossier compressé `.zip`.
3.  **Upload :** * Allez dans **Settings > Widgets** dans votre console Zoho Creator.
    * Cliquez sur **Create** et uploadez le fichier `.zip`.
    * Choisissez l'hébergement **Internal** et définissez `index.html` comme **Index File**.
4.  **Intégration :** Dans l'éditeur de page de votre application, glissez l'élément **Widget** et sélectionnez celui-ci.

## 📝 Utilisation (Test)

* **Mode Succès :** Tapez le mot `CORRECT` (en majuscules) puis appuyez sur **Entrée**.
    * *Résultat :* Message vert + Bip aigu.
* **Mode Échec :** Tapez n'importe quoi d'autre.
    * *Résultat :* Message rouge + Buzz grave.
