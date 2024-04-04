# Config-Dolibarr
Détails de configuration d'un dolibarr pour petit artisan - Niveau Newbie

# Prérequis / contexte
On part d'une instance vierge, installée sur un serveur, en mode admin / super-admin
On a pas la main sur le serveur
On veut configurer l'instance à l'usage d'une TPE artisanale du batiment, hypothétiquement avec un futur fonctionnement en coopérative. Ce sont des entreprises commerciales vendant des ouvrages, un mix de produits et de service.

# Activation des modules nécessaires à l'instance
Cette étape semble devoir être réalisée rapidement, afin de donner les permissions aux groupes une fois pour toute, plutôt que au fur et à mesure de l'activation des modules
Cela implique de connaître les modules nécessaires et leur fonctionnement, donc bien connaître ses besoins aussi

Modules activés au 04/04/2024 :
  Gestion du Dolibarr : Utilisateurs et Groupes
  + Externe : Multi-société : https://www.dolistore.com/fr/modules/69-Multi-soci--t--.html (dans le cas du fonctionnement en coopérative)

  CRM : Tiers + Propals + Facture/Avoirs + Taxes (TVA) + Marge + Produits + Services + externe : 
    Ouvrage/Forfait v5 --> https://www.dolistore.com/fr/modules/1930-Ouvrage-Forfait-v5.html?search_query=btp&results=6
--> La base minimale !
    Autres modules utiles suivant le métier : Stock + Fournisseur + Abonnement/Contrat (entretien)
  ## Tips Config des modules : 
    https://www.dolibarr.fr/forum/t/tiers-particulier/33146 + Dans Accueil > Configuration > Affichage > « Ordre affichage prénom/nom »
  
  Secrétariat et suivi administratif : 
    Compta : Banque/Caisse + Comptabilité partie double
--> pour le suivi financier
    Autres modules utiles ? Gestion des ressources humaine + Congés + Salaires ?

  Suivi de chantier : Projets/Opportunité (à configurer et adapter pour le batiment) + Doc2Project + Externe : 
    Suivi de chantier V4 : https://www.dolistore.com/fr/modules/1741-Suivi-des-chantiers-BTP-V4--.html?search_query=BTP&results=6
    --> Permet la coordination, les rapports de chantier, etc ?
  

# Création de groupes d'utilisateurs
Trois groupes pour le moment : Informaticiens, Gestionnaires et Ouvriers, + Coordinateurs au cas où..


# Importation des données
L'enjeu est maintenant de remplir la base de donnée avec les informations disponibles, spécifiques à chaque entreprise
Quel est le meilleur ordre pour procéder ? 
  1. Tiers puis contacts ?
  2. Produits, services puis ouvrages ?
  3. Devis + Factures (dépendent des points 1 et 2, comment gérer ces dépendances à l'import ?)
  4. Tiers fournisseur puis Plan comptable ? ou inversement ?
  5. Création de projets / suivi de chantier + timesheet pour les ouvriers, tester la fonction suivi de projet coté ouvrier et coté gestionnaires, tester l'appli smartphone
