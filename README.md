# Catalogue-de-20-controles-
Catalogue de 20 contrôles basés sur ISO27001 afin de piloter la conformité et la sécurité de manière mesurable et homogène. 
Les contrôles intègrent implicitement la démarche ISO 27005 et sont réalisés sur un SI hybride AWS et on-premise Microsoft.

14 contrôles ISO/documentaires pour vérifier la conformité du SMSI, les politiques et faire les revues
6 contrôles techniques pour s'assurer de la bonne configuration d'AWS, de l'IAM, de la GPO et d'autres actifs sensibles comme Splunk et la CI/CD.

Contrôles 
_______________________________________________________________________________________________________________________
### Contrôle 1. Gouvernance : Politique SSI de tous les périmètres du SI, ainsi que les applications SaaS de nos fournisseurs. 

Menace couverte : filiales et partenaires comme porte d'entrée. 
Criticité : haute. Réf ISO 27001 A.5.1. Maturité cible : 5. Méthode de vérification Revue politique, fournisseurs.

### Contrôle 2. Gestion des risques : Registre ISO 27005 incluant les nouvelles menaces liées à l'évolution du SI. 

Menaces couvertes : phishing, deepfake, dépendances logicielles. 
Criticité : haute. Réf ISO 27001 A.5.4. Maturité cible : 5. Méthode de vérification Analyse de risques actualisée.

### Contrôle 3. Gestion des identités : Vérification des politiques de MFA sur OKTA et de Zero Trust sur l'AD et AWS IAM. 

Menace couverte : Compromission d'accès SaaS et des politiques IAM. 
Criticité : haute. Réf ISO 27001 A.5.15 et A.5.18. Maturité cible : 5. Méthode de vérification Tests d'authentification, vérification des politiques mis en place dans OKTA, échantillonage de logs. 

### Contrôle 4. CI/CD et DevSecOps : Revue des pipelines GitHub-Lambda et scan des dépendances (artefacts interdits, SBOM, CMDB).

Menace couverte : Compromission via la supply chain logicielle (npm, package infectés). 
Criticité : haute. Réf ISO 27001 A.8.25. Maturité : 5. Méthode de vérification Audit CI/CD et contrôle de code.

### Contrôle 5. Sécurité des actifs SaaS : Surveillance et couverture des accès des API et applications SaaS. Configuration et politiques des moyens d'authentification et solutions SSO et MFA.

Menace couverte : Compromission SaaS et API exposées. 
Criticité : haute. Réf ISO 27001 A.8.16/A.5.17. Maturité : 4. Méthode de vérification Logs d'accès et audit de permissions.

### Contrôle 6. Phishing et Sensibilisation : Campagne de phishing ainsi qu'au quishing/vishing.

Menace couverte : Phishing, deepfake, social engineering. Criticité : haute. Réf ISO 27001 A.6.3. Maturité : 5. Méthode de vérification Résultats des tests de phishing N-1, test de phishing et formation (elearning, webinar).

### Contrôle 7. Supervision et SOC : SIEM Splunk, périmètres couverts et règles mises en places (corrélation sur les accès anormaux, alertes levées, procédure d'escalade des incidents). 

Menace couverte : évolution de la rapidité des attaques grâce à des solutions d'IA. Criticité : haute. Réf ISO 27001 A.8.16. Maturité : 5. Méthode de vérification RETEX des exercices de crise, rejeu des crises, audit de la corrélation des logs parsés au SIEM, procédure d'escalade en cas d'incident.

### Contrôle 8. Gestion des sauvegardes : Sauvegardes isolés, immuables à tester régulièrement (supports, environement et périmètre, délais des sauvegardes). 

Menace couverte : Indisponibilité ou suppression des sauvegardes. Criticité : haute. Réf ISO A.8.13. Maturité : 5. Méthode de vérification test PRA, air gap et redondance de l'environement AWS dans une autre zone.

### Contrôle 9. Sécurité des données : Politique de chiffrement (KMS, TDE, TLS, gestion des clefs de chiffrement) en fonction de la criticité des périmètres.

Menace couverte : Confidencialité de la donnée. Criticité : Haute. Réf ISO 27001 A.8.24. Maturité : 5. Méthode de vérification Politique de chiffrement, revue des configurations et gestion des clefs de chiffrement.

### Contrôle 10. Gestion des vulnérabilités : Procédure de patching, comité de triage (priorisation de traitement des vulnérabilités et du traitement des faux positifs) et veille.

Menace couverte : Exploitation des vulnérabilités des actifs sensible et de sécurité. Criticité : Haute. Réf ISO 27001 A.8.8. Maturité : 5. Méthode de vérification Procédure de gestion des vulnérabilités, compte rendu des comités de triage, reporting du suivi des vulnérabilités à la direction, échantillon des scans de vulnérabilités et résultat des bug bounty en N-1.

### Contrôle 11. Contrôle des accès à privilèges (PAM) : Journalisation, session recording, contrôle des accès, politique des PAM. 
Menace couverte : combinaison toxique (lutte contre la fraude interne), escalade de comptes administrateurs, ADCS (serveur de certificat, CA racine ou subordonnée) compromis. Criticité : Haute. Réf ISO 27001 A.5.18. Maturité : 5. Méthode de vérification Revue des comptes, contrôle annuel des accès et politique PAM.

### Contrôle 12. Sécurité réseau : Segmentation VPC/VPN/DMZ, audit des flux entrants (règles de routage/firewall et EDR). 

Menace couverte : intrusion via VPN, déplacements latéraux. Criticité : Haute. Réf ISO 27001 A.8.20. Maturité : 4. Méthode de vérification Revue firewall, EDR, VPC flow logs.

### Contrôle 13. Gestion des tiers : Audit de sécurité des tiers et des filiales (Contrôle permanent, demande de Plan d'Assurance Sécurité, audits externes). 

Menace couverte : attaque supply chain. Criticité : Haute. Réf ISO 27001 A.5.19. Méthode de vérification Revue des contrats, audits des tiers.

### Contrôle 14. Sécurité applicative : Test d'intrusion avant mise en production, code review, couverture du périmètre par le WAF. 

Menace couverte : Vulnérabilité web et de code (exemple : XSS, Log4j). Criticité : Haute. Réf ISO 27001 A.8.9. Maturité : 4. Méthode de vérification Rapport de pentests, Scan de code, configuration du WAF.

### Contrôle 15. Gestion d'incident : Procédure de réponse à incident en rapport avec l'évolution de la menace en N-1. 

Menace couverte : Attaque automatisées, deepfake, usurpation du support informatique (helpdesk). Criticité : Moyenne. Réf ISO 27001 A.5.24. Maturité : 4. Méthode de vérification Retex des rejeux d'incident, exercice de crise, procédure de la remontée des incidents au SOC. 

### Contrôle 16. Surveillance des applications SaaS : Couverture des accès, logs des solutions de monitoring des accès avec SSO et MFA, détection des comportements (UEBA).

Menace couverte : usurpation de compte utilisateur et administrateur, escalade des privilèges. Criticité : Moyenne. Réf ISO 27001 A.8.16. Maturité : 4. Méthode de vérification Analyse de log, revue et contrôle des accès et habilitations. 

### Contrôle 17. Continuité d'activité (résilience) : PRA/PCA testés avec les scénarios les plus critiques impliquant les actifs vitaux pour l'activité.

Menace couverte : Ransomware, attaque éclair, suppression de sauvegarde. Criticité : Haute. Réf ISO 27001 A.5.29. Maturité : 5. Méthode de vérification Retex exercide de crise PCA/PRA, procédure d'escalade en cas d'incident sur les périmètres sensibles.

### Contrôle 18. Cryptographie : Rotation des clefs , gestion des secrets, protocoles de chiffrement et de hachage utilisés. 

Menace couverte : Exfiltration des clefs et des secrets. Criticité : Haute. Réf ISO 27001 A.8.24. Maturité : 4. Méthode de vérification Audit de gestion des clefs et des secrets, ainsi que les protocoles utilisés.

### Contrôle 19. Sensibilisation étendue : formation des équipes aux nouvelles menaces (exemple deepfake).

Menace couverte : nouvelles menaces comme le deepfake, usurpation des dirigeants. Criticité : Moyenne. Réf ISO 27001 A.6.3. Maturité : 3. Méthode de vérification : Formation, reporting RH.

### Contrôle 20. Amélioration continue : Revue de direction intégrant les menaces émergentes (évolution de la posture de la cybersécurité).

Menace couverte : Adaptation aux nouveaux risques. Criticité : Moyenne. Réf ISO 27001 A.10.1. Maturité : 4. Méthode de vérification Compte rendu des revues de la direction.
