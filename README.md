# Catalogue-de-20-controles-
Catalogue de 20 contrôles basés sur ISO27001 afin de piloter la conformité et la sécurité de manière mesurable et homogène. 
Les contrôles intègrent implicitement la démarche ISO 27005 et sont réalisés sur un SI hybride AWS et on-premise Microsoft.

14 contrôles ISO/documentaires pour vérifier la conformité du SMSI, les politiques et faire les revues
6 contrôles techniques pour s'assurer de la bonne configuration d'AWS, de l'IAM, de la GPO et d'autres actifs sensibles comme Splunk et la CI/CD.

Contrôles 
_______________________________________________________________________________________________________________________
Contrôle 1. Gouvernance : Politique SSI de tous les périmètres du SI, ainsi que les applications SaaS de nos fournisseurs. 

Menace couverte : filiales et partenaires comme porte d'entrée. 
Criticité : haute. Réf ISO 27001 A.5.1. Maturité cible : 5. Méthode de vérification Revue politique, fournisseurs.

Contrôle 2. Gestion des risques : Registre ISO 27005 incluant les nouvelles menaces liées à l'évolution du SI. 

Menaces couvertes : phishing, deepfake, dépendances logicielles. 
Criticité : haute. Réf ISO 27001 A.5.4. Maturité cible : 5. Méthode de vérification Analyse de risques actualisée.

Contrôle 3. Gestion des identités : Vérification des politiques de MFA sur OKTA et de Zero Trust sur l'AD et AWS IAM. 

Menace couverte : Compromission d'accès SaaS et des politiques IAM. 
Criticité : haute. Réf ISO 27001 A.5.15 et A.5.18. Maturité cible : 5. Méthode de vérification Tests d'authentification, vérification des politiques mis en place dans OKTA, échantillonage de logs.   
