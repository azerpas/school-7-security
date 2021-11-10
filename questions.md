## Chapitre 0

### Définition de la sécurité
L'ensemble des moyens techniques, humains et organisationnels mis en oeuvre pour protéger un SI et le patrimoine de l'entreprise.
### Les 3 familles de mesures de sécurité
### Définition des 4 critères de sécurité
- Disponibilité:
- Intégrité:
- Confidentialité:
- Traçabilité:
### Notion de « besoin d’en connaître »
Rattaché à la notion de confidentialité. Seuls les personnes concernées peuvent connaître le contenu.
### Définition d’un incident de sécurité
Tout évènement qui entraîne la baisse d'un des 4 critères de sécurité
### Les types d’incidents
- Malveillance externe
- Malveillance interne
- L'erreur
- Le dysfonctionnement
### Les types d’impacts
- Financier
- Juridique
- Réputation
- Humain
### La notion d’APT
Advanced Persistent Threats: Techniques pour rester dans le SI

## Chapitre 1: Introduction

### Quelle est la référence de l’Etat en matière de SSI?
ANSSI
### Que représentent des CVE, CVSS?
- Common Vulnerabilities and Exposures
- Common Vulnerabilities Scoring System
### Les 4 raisons de faire de la sécurité
- On veut: **Normes**
- On est obligé: **Lois**
- On nous le demande: **Bonnes pratiques**
- Ça rapporte: **ROI**
### Contenu d’une PSSI
Politique de sécurité:
- Définition du périmètre
- Responsabilités des SSI
- Définition des objectifs de sécurité
- Analyse de risque
- Description contrôles et audits
### Qu’est-ce qu’un risque résiduel?
On ne peut pas tout protéger, on accepte donc le risque.
### Principe du PDCA
De l'itération
- Planifier 
- Développer
- Checker
- Ajuster

## Chapitre 2: Droit et NTIC

### Loi informatique et libertés
### Rôle de la CNIL
### Quel est le domaine de la HADOPI
### Liberté et gratuité
### Licence copyleft

## Chapitre 3: L'analyse et le risque

### Les 2 méthodologies d’analyse de risques
### La norme ISO de gestion des risques
27005
### Vocabulaire: vulnérabilité, menace et risque
- Menace: cause probable d'un incident de sécurité
- Vulnérabilité: faille qui peut être exploitée par menace
- Risque: probabilité de réalisation d'une menace
### Notion de risque résiduel
On ne peut pas tout protéger, on accepte donc le risque.

## Chapitre 4: Architectures sécurisées

### Défense en profondeur
Plusieurs lignes de défense: plusieurs Firewall, DMZ, habilitations...
### Principe de moindre privilège
Pour traverser une défense en profondeur:
- l'utilisateur être autorisé
- la fonction doit être prévue

## Chapitre 5: Gestion des identités et des accès

### Définir « identification », « authentification » et « autorisation »
- Identification: Obtenir l'identité de l'utilisateur
- Authentification: Vérifier l'identité de l'utilisateur
- Autorisation: Vérifier si l'utilisateur a accès 
### Faire la différence entre authentification simple, double et forte
- Simple: un critère
- Multiple: plusieurs authentifications
- Forte: au moins deux critères et un élément cryptographique
### Fédération d’identité
Ressources font confiance dans un tiers par rapport au client.
- Kerberos: ticket donne droit d'accès temporaire
- SAML: jeton montre que user est authentifié
### LDAP
Lightweight Directory Access Protocol
- Un arbre...
  - ... d'entrées...
    - ... avec des attributs:
      - nom
      - type
      - valeurs
- Opérations:
  - Bind (login)
  - Search
  - Add / Delete / Modify

## Chapitre 6: Durcissement

### Dans tous les cas, une cartographie s’impose
### Notion de « règles d’hygiène »
- Cartographie précise de l'installation informatique
- MAJ des composants logiciels
- Limiter supports amovibles
- Chiffrer données
### Durcissement des dev. D’applications:
#### Audits de code
- Disponibilité: robustesse, tests de montée en charge
- Intégrité: contrôles de saisie
- Confidentialité: chiffrement des flux
- Traçabilité: logs
#### Références de l'OSWAP
- Injection
- Auth et sessions
- XSS (Cross Site Scripting)
- Données sensibles

## Chapitre 7: Cryptographie (pas noté)

### Cryptographie / stéganographie
### Faire la différence: chiffrement, déchiffrement,  décryptage
### Symétrique / asymétrique
### Clé publique / clé privée

## Chapitre 8: Infrastructures à clé publique "PKI"

### Que représente X509?
### Définition et rôle: AC, AE?
### Qu’est-ce qu’une « chaîne de certification »?
### Qu’est-ce qu’un certificat « autosigné »?
### Pourquoi un certificat autosigné est-il peu sûr?

## Chapitre 9: Gestion quotidienne de la sécurité des SI

### Contenu de la PSSI
### Grands principes de la crise: 
#### RPO, RTO, WRT, MTD

## Chapitre 10: Normes de sécurité et audits

### Normes spécifiques: PCI-DSS, ISO 2700x

## Chapitre 11: Grands enjeux actuels
