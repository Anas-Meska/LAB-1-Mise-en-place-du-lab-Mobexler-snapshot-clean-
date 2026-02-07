# LAB 1 – Mise en place du lab Mobexler (Snapshot Clean)

##  Objectif du TP

L’objectif de ce laboratoire est de mettre en place un environnement Mobexler fonctionnel sous VirtualBox, de vérifier la connectivité réseau, de configurer l’USB pour Android (ADB), puis de créer un snapshot propre (**Clean Baseline**) prêt pour les futurs travaux pratiques.

---

##  Environnement utilisé

- **Hyperviseur** : Oracle VirtualBox  
- **Machine virtuelle** : Mobexler (Debian 64-bit)  
- **Réseau** : NAT + Host-Only  
- **Téléphone Android** : Infinix HOT 60 Pro+  
- **Outil Android** : ADB  

---

## 1️ Importation de la machine virtuelle Mobexler

La machine virtuelle Mobexler est importée avec succès dans Oracle VirtualBox.  
Le système d’exploitation détecté est **Debian (64-bit)**.  

Les ressources matérielles (mémoire RAM, processeur et espace disque) sont vérifiées et jugées suffisantes pour assurer le bon fonctionnement de l’environnement Mobexler.

---

## 2️ Configuration réseau – Adapter 1 (NAT)

L’interface réseau **Adapter 1** est activée et configurée en mode **NAT**.  

Cette configuration permet à la machine virtuelle d’accéder à Internet via la connexion de la machine hôte, ce qui est nécessaire pour les mises à jour système et les tests de connectivité.

---

## 3️ Configuration réseau – Adapter 2 (Host-Only)

L’interface réseau **Adapter 2** est activée et configurée en mode **Réseau privé hôte (Host-Only)**.  

Ce mode permet la communication directe entre la machine virtuelle et la machine hôte, tout en restant isolé du réseau externe.

---

## 4️ Démarrage et connexion à Mobexler

La machine virtuelle Mobexler démarre correctement.  
L’accès à l’interface utilisateur est réussi, confirmant que le système d’exploitation fonctionne normalement après l’importation et la configuration réseau.

---

## 5️ Vérification de la configuration réseau

### Table de routage

La commande de vérification de la table de routage montre la présence d’une route par défaut via l’interface **NAT**, indiquant une configuration réseau correcte.

### Test de connectivité Internet

Les tests de connectivité vers une adresse IP publique et un nom de domaine confirment que la machine virtuelle dispose d’un accès fonctionnel à Internet.

### Vérification des interfaces réseau

Les interfaces réseau actives disposent d’adresses IP valides, ce qui confirme le bon fonctionnement des configurations **NAT** et **Host-Only**.

---

## 6️ Création du snapshot CLEAN_BASELINE_TP1

Un snapshot nommé **CLEAN_BASELINE_TP1** est créé.  

Ce snapshot correspond à un état stable du système, avec :
- Importation validée  
- Réseau NAT et Host-Only fonctionnels  
- Démarrage correct de la VM  
- Environnement prêt pour l’utilisation d’ADB  

Il servira de point de restauration pour les futurs travaux pratiques.

---

## 7️ Configuration USB et ADB (Android)

Les options développeur ainsi que le **débogage USB** sont activés sur le téléphone Android.  

Le téléphone **Infinix HOT 60 Pro+** est ajouté comme périphérique USB dans VirtualBox afin d’être reconnu par la machine virtuelle.

Le service ADB est ensuite démarré et vérifié.  
Le périphérique Android apparaît avec l’état **device**, ce qui confirme que la communication entre Mobexler et le téléphone est fonctionnelle.

---

##  Conclusion

À l’issue de ce laboratoire :

- La machine virtuelle Mobexler est correctement installée  
- La connectivité réseau est opérationnelle  
- La communication Android via ADB est fonctionnelle  
- Un snapshot propre (**Clean Baseline**) est disponible  

L’environnement est prêt pour les futurs travaux pratiques et analyses Android.
