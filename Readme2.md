Objectif de l'exercice : Automatiser le déploiement d'une application web sur un serveur Linux à l'aide de Jenkins.

Prérequis :

Jenkins installé et configuré :
  Un serveur Linux accessible depuis Jenkins avec les droits nécessaires.
  Une application web avec un code source géré dans un système de contrôle de version, comme Git.
  
Étapes de l'exercice :
  Configuration de Jenkins :
    Assurez-vous que Jenkins est correctement installé et en cours d'exécution.
    Installez les plugins nécessaires, tels que le plugin Git et le plugin SSH.
    
Création d'un nouveau travail Jenkins :
  Créez un nouveau travail Jenkins de type "Projet freestyle".
  Configuration des paramètres généraux :
  Donnez un nom au travail (par exemple, "Déploiement de l'application web").
  Configurez les déclencheurs pour déclencher le travail lorsque des modifications sont détectées dans votre référentiel Git.
  
Gestion du code source :
Dans la section "Gestion de code source", sélectionnez Git.
  Configurez les informations de votre référentiel Git (URL, identifiants, branche à surveiller, etc.).

Actions de construction :
Dans la section "Build", ajoutez les étapes nécessaires pour le déploiement de l'application. Cela peut inclure :
  Récupération du code source depuis Git.
  Compilation de l'application (si nécessaire).
  Copie des fichiers de l'application vers le serveur Linux via SSH.
  Redémarrage du serveur web pour appliquer les modifications.
  Nettoyage des fichiers temporaires sur le serveur.
  
Gestion des erreurs :
Configurez des étapes pour gérer les erreurs éventuelles, telles que des échecs de compilation ou des erreurs de déploiement. Vous pouvez envoyer des notifications par e-mail en cas d'échec.

Actions postérieures à la construction (facultatif) :
Dans la section "Actions postérieures à la construction", configurez des actions telles que l'envoi de notifications de déploiement réussi, la publication de rapports de déploiement, etc.

Sauvegarde et test :
Enregistrez la configuration du travail Jenkins.
Lancez manuellement le travail pour vérifier que le déploiement fonctionne correctement.

Automatisation complète :
Vous pouvez automatiser davantage en utilisant des scripts et des variables d'environnement pour gérer différents environnements de déploiement (développement, pré-production, production).
Surveillance :

Mettez en place une surveillance pour vérifier régulièrement que l'application est accessible après le déploiement.
Cet exercice vous permettra de mettre en place un processus d'intégration continue (CI) pour votre application web, ce qui signifie que chaque fois qu'une nouvelle version de l'application est poussée dans le référentiel Git, Jenkins l'automatisera jusqu'au déploiement sur le serveur Linux cible.
