📌 Rapport d'Automatisation - Extraction et Manipulation de Données avec UiPath
📖 Introduction
Ce projet décrit un flux d'automatisation développé avec UiPath, utilisant des techniques avancées d'extraction et de manipulation de données à partir d'un site e-commerce. L'objectif est d'assurer une extraction rapide, efficace et robuste, garantissant que les données soient correctement traitées et stockées dans un fichier Excel.

🛠️ Technologies Utilisées
UiPath : Plateforme d'automatisation utilisée pour le développement du flux.
LINQ : Utilisé pour la manipulation et le filtrage des données.
VBA : Employé dans certaines étapes spécifiques pour améliorer les performances.
🔢 Variables du Flux
Le flux utilise les variables suivantes :

String :

linkURL : Stocke le lien du site à utiliser.
Base de données :

Database_Extraida : Contient les informations extraites du site.
Output_Database : Contient uniquement les noms et la moyenne des prix.
Booléennes :

boolSite : Indique si une erreur s'est produite lors du chargement du site.
validadorSite : Vérifie si le site a été correctement chargé.
⚙️ Structure du Flux
1️⃣ Navigation sur le Site Web
Ouverture du Navigateur : Utilisation d'un connecteur pour ouvrir Edge et naviguer vers le lien fourni.
Validation du Chargement : Vérification et rechargement si nécessaire.
Accès à la catégorie "Phones" : Vérification et interaction avec le menu.
Validation du Rechargement : Logique mise en place pour assurer que le menu reste accessible malgré le rechargement du site.
2️⃣ Processus d'Extraction des Données
Utilisation des activités d'extraction de données UiPath AI pour récupérer les colonnes suivantes :
🏷️ Nom
💰 Prix
📝 Description
⭐ Nombre d'avis
3️⃣ Manipulation des Données
Conversion du champ "Prix" en format numérique pour faciliter les calculs.
Tri du champ "Nombre d'avis" par ordre décroissant pour faciliter l'analyse.
4️⃣ Stockage et Calcul
Les données sont stockées dans Output_Database.
Calcul de la moyenne des prix.
📂 Validation et Stockage des Données
Avant d'enregistrer les données dans Excel, le flux vérifie si des données ont bien été extraites :

Si aucune donnée n'est extraite, le processus s'arrête.
Sinon, les informations sont enregistrées dans un fichier Excel avec :
Feuille 1 : Données extraites (Nom, Prix, Description, Nombre d'avis).
Feuille 2 : Moyenne des prix calculée.
📊 Journalisation des Erreurs et Avertissements
Des logs sont mis en place pour assurer la fiabilité du flux :

Début du processus : Journal indiquant le lancement du flux.
Erreurs capturées :
Problèmes de navigation
Données manquantes
Échecs de chargement des pages
🚀 Performance et Efficacité
✅ Optimisation : Le processus s'exécute en 45 secondes.    
✅ Temps d'attente stratégiques (Wait) pour assurer le chargement complet des pages avant l'extraction.

📌 Observations Complémentaires
Langue : Développement effectué en portugais, mais les annotations et traductions sont intégrées pour assurer la compréhension dans toutes les versions d'UiPath
