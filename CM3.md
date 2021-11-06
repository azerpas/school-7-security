# Architecture

## Origines
- Principe de la "muraille de Chine"      
	**Défense périmétrique**, perçant un niveau puis en se propageant.
- Principe de "défense en profondeur"     
	Plusieurs lignes de défense, e.g: plusieurs firewall l'un derrière l'autre

## Concepts
- "Le renseignement est la première ligne"
	- **Traduction SI**: Veille techno maintient à jour évolution menaces
- "Chq ligne de déf a un rôle"
	- **Traduction IT**: Chq élément a son rôle
	- *Exemple*: firewall sert à cloisonner, pas routage
- "On doit traiter menaces externes et internes"
	- **Traduction IT**: attaquant ext ou intérieur
	- *Exemple*: Contrôle d'accès
- "Chq ligne est autonome"
	- **Traduction IT**: chq él de protection doit avoir propre efficacité et propre protection
	- *Exemple*: équipement de filtrage doit avoir contrôle d'accès
- "Défense en profondeur doit être démontrée"
	- **Traduction IT**: les éléments de défense doivent ê testés et revalidés 

## Analyse fonctionnelle
- On découpe l'archi en blocs fonctionnels
	1. Première approche puis raffinements
	2. Définition de niveaux de sensibilité
	3. Définition de critères de sécu
- On définit les liens et protections 
	1. Liens entre extérieur et sys
	2. Liens des blocs fonctionnels entre eux
	3. Liste de besoins de cloisonnement

## Architecture 3 tiers
### Couche présentation
- Analyse des requêtes mal formées
- Neutralisation des données à afficher
### Couche application
- Validation de la cohérence des données traitées
- Habilitations des utilisateurs
### Couche données
- Gestion fine des droits applicatifs
- Procédures de sauvegarde/restauration

## Besoin d'en connaître
- Notion de "moindre privilège"
Pour avoir droit de traverser une couche de défense en profondeur
	- La fonction doit être prévue
	- L'utilisateur (le compte) concerné 

## Cloisonnement vs. Accès
- Je peux accéder à une ressource
- J'ai le droit d'accéder à une ressource

# Gestion des environnements
## Cloisonnement en "DMZ"
Isoler un ss-réseau des autres, au moyen d'équipements de filtrage (firewall)
- DMZ "complexe": 2 FW et 2 interfaces
	- En cas d'attaque, un FW est compromis
	- Si saturation du FW externe, le FW interne continue à servir utilisateurs interne
## Contenu des zones
- **Zone non-contrôlée**: réseau non sûr, Internet
- **Zone DMZ**: load balancer, reverse proxy, ...
- **Zone restreinte**: élémts de productions, base de données
- **Zone intranet**: postes de travail
- **Zone sécurisée**: administration ou zone sensible

## Cloisonner l'administration
- Solution 1: des réseaux dédiés
- Solution 2: réseau physique mutualisé mais chiffrement matériel
- Solution 3: réseau mutualisé et VPN poste de travail
### Bastion d'administration 
Point d'entrée unique.
- __Sécurité de l'accès__: contrôle d'accès robustes, droits fins
- __Sécurité dans les tâches d'administration__: commandes et outils accessibles
- __Sécurité de cloisonnement__: zone réseau, tampon, pas de rebond possible
### Isolation réseau
Logique du NAC
- ACL spécifique de blocage sur les routeurs
- Blocage au niveau DHCP
- Blocage au niveau ARP

À retenir
- Défense en profondeur
- DMZ schéma
- FW successifs schémas
- Point d'accès Internet schéma (deux chaînes)

