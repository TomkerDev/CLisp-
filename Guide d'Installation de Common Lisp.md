# Guide d'Installation de Common Lisp sur Windows 10

## 1. Choix de l'Implémentation
Pour débuter, nous recommandons **SBCL (Steel Bank Common Lisp)**, une implémentation populaire et performante.

D'autres options incluent :
- **SBCL (Steel Bank Common Lisp)** : rapide et largement utilisé.
- **CLISP** : compatible multi-plateforme mais légèrement plus lent.

Pour simplifier, ce guide se concentrera sur l’installation de **SBCL**.

---

## 2. Télécharger SBCL
1. Rendez-vous sur le [site officiel de SBCL](http://www.sbcl.org/).
2. Dans la section **Binaries**, choisissez la version pour Windows et téléchargez le fichier `.msi` (installateur Windows).

---

## 3. Installer SBCL
1. Ouvrez le fichier `.msi` téléchargé et suivez les instructions de l’assistant d’installation.
2. Notez ou conservez l'emplacement d'installation par défaut, souvent `C:\Program Files\Steel Bank Common Lisp`, car ce chemin sera utilisé pour configurer les variables d'environnement.

---

## 4. Configurer les Variables d'Environnement
Pour rendre SBCL accessible depuis n'importe quel terminal ou éditeur, ajoutez le chemin d'installation à la variable d'environnement **PATH**.

### Étapes :
1. **Ouvrir les Paramètres Système** :
   - Faites un clic droit sur **Ce PC** (ou **This PC**) et sélectionnez **Propriétés**.
   - Dans le menu de gauche, cliquez sur **Paramètres système avancés**.
   - Dans la fenêtre des propriétés système, cliquez sur **Variables d'environnement**.

2. **Ajouter SBCL à PATH** :
   - Dans la section **Variables système**, recherchez `Path`, sélectionnez-la, puis cliquez sur **Modifier**.
   - Cliquez sur **Nouveau** et ajoutez le chemin d'installation de SBCL, par exemple :
     ```
     C:\Program Files\Steel Bank Common Lisp\sbcl
     ```
   

3. **Enregistrer et Fermer** :
   - Cliquez sur **OK** pour fermer chaque fenêtre et enregistrer les modifications.

---

## 5. Vérifier l'Installation
Pour confirmer que SBCL est bien installé et que la variable d'environnement est correctement configurée :

1. **Ouvrez l'invite de commande (cmd)** :  
   - Tapez **cmd** dans la barre de recherche Windows et ouvrez l'invite de commande.
   
2. **Vérifiez SBCL** :
   - Dans la fenêtre de commande, tapez :
     ```cmd
     sbcl
     ```
   - Si tout est correctement configuré, l’interpréteur SBCL s'ouvre et affiche un message d'accueil.

3. **Test de Fonctionnement** :
   - Exécutez une simple commande Lisp pour vérifier le bon fonctionnement :
     ```lisp
     (print "Hello, world!")
     ```
   - Si `"Hello, world!"` apparaît, l'installation est réussie.

---

## 6. Configuration dans Visual Studio Code avec l'Extension Common Lisp
Pour utiliser SBCL avec Visual Studio Code :

1. **Installez Visual Studio Code** depuis le [site officiel](https://code.visualstudio.com/).
2. **Ajoutez l'extension "Common Lisp"** :
   - Ouvrez Visual Studio Code, puis accédez au **Marketplace** des extensions (icône en forme de carré dans la barre latérale).
   - Recherchez **Common Lisp** et installez l'extension correspondante.

3. **Lancer une session Common Lisp** :
   - Créez ou ouvrez un fichier avec l'extension `.lisp` dans Visual Studio Code.
   - Utilisez la commande **Run Lisp** (disponible dans la barre de commandes de Visual Studio Code) pour lancer une session et exécuter votre code Common Lisp.

---

Votre environnement **Common Lisp** est désormais prêt à être utilisé dans **Visual Studio Code** avec **SBCL**.
*@TomkerDev*