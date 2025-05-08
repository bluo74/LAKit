# LaKit

**LaKit** est un plugin utilitaire pour les serveurs basés sur le framework **Life**. Il fournit des outils pour gérer les fichiers JSON, personnaliser les textes, envoyer des notifications et des messages aux joueurs, et bien plus encore.

---

## **Fonctionnalités principales**
- **Gestion des fichiers JSON** : Sauvegarde et chargement de données au format JSON.
- **Personnalisation des textes** : Ajout de couleurs, tailles et styles aux textes.
- **Notifications** : Envoi de notifications d'information, d'erreur, de succès ou d'avertissement aux joueurs.
- **Messages** : Envoi de messages aux joueurs, à tous les joueurs ou uniquement aux administrateurs.

---

## **Installation**
1. Clonez ou téléchargez ce dépôt.
2. Placez le dossier `LaKit` dans le répertoire `Plugins` de votre serveur.
3. Assurez-vous que toutes les dépendances nécessaires (comme `Newtonsoft.Json`) sont disponibles.

---

## **Utilisation**
### **1. Gestion des fichiers JSON**
La classe `JsonHelper` permet de sauvegarder et charger des données au format JSON.

#### **Exemple : Sauvegarder des données**
JsonHelper.Save(new { Name = "Exemple" }, "ExempleFichier");

#### **Exemple : Charger des données**
var data = JsonHelper.Load<object>("ExempleFichier");

#### **Définir un chemin personnalisé**
JsonHelper.SetCustomPath("C:\Serveur\Plugins\NovaLifeServer");

---

### **2. Personnalisation des textes**
La classe `TextHelper.Color` permet de colorer les textes, et la méthode `Size` permet de définir leur taille.

#### **Exemple : Texte coloré**
string texteRouge = TextHelper.Color.Red("Ceci est un texte rouge"); string texteVert = TextHelper.Color.Green("Ceci est un texte vert"); string textePersonnalise = TextHelper.Color.Custom("FF5733", "Texte orange");

#### **Exemple : Texte avec taille personnalisée**
string texteGrand = TextHelper.Size(24, "Texte en taille 24");

---

### **3. Notifications**
Envoyez des notifications aux joueurs avec différents types (Info, Erreur, Succès, Avertissement).

#### **Exemple : Notification d'information**
TextHelper.NotifyInfo(player, "Titre", "Ceci est une notification d'information.");

#### **Exemple : Notification d'erreur**
TextHelper.NotifyError(player, "Erreur", "Une erreur est survenue.");


---

### **4. Messages**
Envoyez des messages aux joueurs ou à des groupes spécifiques.

#### **Exemple : Message à un joueur**
TextHelper.Message(player, "Bienvenue sur le serveur !");

#### **Exemple : Message à tous les joueurs**
TextHelper.MessageToAll("Le serveur redémarrera dans 5 minutes.");

#### **Exemple : Message aux administrateurs**
TextHelper.MessageToAllAdmin("Un joueur a été banni.");

---

## **Licence**
Ce projet est sous licence MIT. Consultez le fichier `LICENSE` pour plus d'informations.

---

## **Contact**
Pour toute question ou suggestion, contactez-nous sur notre Discord : [L.A Studio](https://discord.gg/F3SufQg7).
