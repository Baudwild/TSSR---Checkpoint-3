## Partie 1 : Gestion des utilisateurs
### Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.
- adduser baudouin

### Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?
- Avoir un mdp fort, comme par exemple 17 caractères.
- Des restrictions au niveaux des droits

## Partie 2 : Configuration de SSH
### Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.
- nano /etc/ssh/sshd.config
- PermitRootLogin no

### Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.
- AllowUsers baudouin

### Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe
-

## Partie 3 : Analyse du stockage
### Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?
- Les fichier montés sont boot et SWAP.

### Q.2.3.2 Quel type de système de stockage ils utilisent ?
- Raid et LVM


### Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID
![image8](/Image8.png)

### Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes.
- 

## Partie 4 : Sauvegardes
### Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.
bareos-dir : Il coordonne et contrôle toutes les opérations de sauvegarde, restauration, vérification et archivage.
bareos-sd : responsable de l'écriture et de la lecture des données sauvegardées sur des dispositifs de stockage.
bareos-fd : stocke ou récupère les données sur/depuis le support de stockage.

## Partie 5 : Filtrage et analyse réseau

## Partie 6 : Analyse de logs
### Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :
- last -f /var/log/wtmp

![image9](/Image9.png)
