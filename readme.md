Par **DECAUDIN Lorenzo** & **MAGALHAES Dylan**
24/11/2023 - v1 - 17h34
Ce document n'est soumise à aucune license de droit.

![Watermark](/assets/Watermark/Wolfy-Tiriel.png)

# Sommaire :
[Installer le rôle Hyper-V sur un serveur Windows](#installez-le-rôle-hyper-v-sur-un-serveur-windows)

[Création de Machines Virtuelles](#création-de-machines-virtuelles)
[Gestion des Machines Virtuelles](#gestion-des-machines-virtuelles)
[Différence entre arrêter et mettre en pause une VM..](#différence-entre-arrêter-et-mettre-en-pause-une-vm)
[Quels paramètres peuvent être modifiés en cours d'exécution ?](#quels-paramètres-peuvent-être-modifiés-en-cours-d'exécution-?)
[Clonez une machine virtuelle existante.](#clonez-une-machine-virtuelle-existante)
[Exportez une machine virtuelle vers un autre emplacement.](#exportez-une-machine-virtuelle-vers-un-autre-emplacement)
[Déplacer une VM avec la migration dynamique](#déplacer-une-vm-avec-la-migration-dynamique)
[Snapshots et Sauvegardes](#snapshots-et-sauvegardes)
[Créez un snapshot de la machine virtuelle.](#créez-un-snapshot-de-la-machine-virtuelle)
[Revenez à un état précédent en utilisant le snapshot](#revenez-à-un-état-précédent-en-utilisant-le-snapshot)
[Configurez une tâche de sauvegarde pour la machine virtuelle.](#configurez-une-tâche-de-sauvegarde-pour-la-machine-virtuelle)
[Réseau Virtuel](#réseau-virtuel)
[Configurez un commutateur virtuel](#configurez-un-commutateur-virtuel)
[Attachez la machine virtuelle à différents réseaux virtuels.](#attachez-la-machine-virtuelle-à-différents-réseaux-virtuels)
[Testez la connectivité](#testez-la-connectivité)
[Surveillance et Gestion à Distance](#surveillance-et-gestion-à-distance)
[Configurez l'accès à distance à Hyper-V Manager à partir d'un autre ordinateur ou Hyper-V.](#configurez-l'accès-à-distance-à-hyper-v-manager-à-partir-d'un-autre-ordinateur-ou-hyper-v)

# Installez le rôle Hyper-V sur un serveur Windows.
**Accéder au "Gestionnaire de serveur"**
![1](/assets/0-Installation%20Hyper-V/1.png)

**Cliquer sur l'onglet "Gérer", puis sur "Ajouter des rôles & fonctionnalités".**
![2](/assets/0-Installation%20Hyper-V/2.png)

**Cliquer sur "Suivant" jusqu'à arriver à l'onglet "Type d'installation".**
![3](/assets/0-Installation%20Hyper-V/3.png)

**Sélectionner "Installation basée sur un rôle ou une fonctionnalité" puis cliquer sur "Suivant".**
![4](/assets/0-Installation%20Hyper-V/4.png)

**Sélectionner le serveur sur lequel vous souhaitez installer le rôle Hyper-V puis cliquer sur "Suivant".**
![5](/assets/0-Installation%20Hyper-V/5.png)

**Sélectionner le rôle "Hyper-V" puis cliquer sur "Suivant".**
![6](/assets/0-Installation%20Hyper-V/6.png)

**Cliquer sur "Ajouter des fonctionnalités" jusqu'à arriver à l'onglet "Confirmation de l'installation".**
![7](/assets/0-Installation%20Hyper-V/7.png)

**Cliquez sur "Suivant".**
![8](/assets/0-Installation%20Hyper-V/8.png)

**Cliquez sur "Suivant".**
![9](/assets/0-Installation%20Hyper-V/9.png)

**Cliquez sur "Suivant".**
![10](/assets/0-Installation%20Hyper-V/10.png)

**Cliquez sur "Suivant".**
![11](/assets/0-Installation%20Hyper-V/11.png)

**Cliquez sur "Installer"**
![12](/assets/0-Installation%20Hyper-V/12.png)

**Le rôle s'installe.**
![13](/assets/0-Installation%20Hyper-V/13.png)

**Cliquez sur "Fermer".**
![14](/assets/0-Installation%20Hyper-V/14.png)

**Le rôle Hyper-V est maintenant installé sur le serveur.**
![15](/assets/0-Installation%20Hyper-V/15.png)
![16](/assets/0-Installation%20Hyper-V/16.png)

## Création de Machines Virtuelles
### Créez une nouvelle machine virtuelle
**Ouvrez le "Gestionnaire Hyper-V".**
![2-1](/assets/1-Création%20de%20Machines%20Virtuelles/2-1.png)

**Cliquez sur "Nouveau" puis sur "Ordinateur virtuel".**
![2-2](/assets/1-Création%20de%20Machines%20Virtuelles/2-2.png)

**Cliquez sur "Suivant".**
![2-3](/assets/1-Création%20de%20Machines%20Virtuelles/2-3.png)

**Nommez votre machine virtuelle puis cliquez sur "Suivant".**
![2-4](/assets/1-Création%20de%20Machines%20Virtuelles/2-4.png)

**Sélectionnez la génération de votre machine virtuelle puis cliquez sur "Suivant".**
![2-5](/assets/1-Création%20de%20Machines%20Virtuelles/2-5.png)

**Sélectionnez la quantité de mémoire vive que vous souhaitez allouer à votre machine virtuelle puis cliquez sur "Suivant".**
![2-6](/assets/1-Création%20de%20Machines%20Virtuelles/2-6.png)

**Sélectionnez le réseau virtuel que vous souhaitez utiliser puis cliquez sur "Suivant".**
![2-7](/assets/1-Création%20de%20Machines%20Virtuelles/2-7.png)

**Sélectionnez "Créer un disque dur virtuel" puis cliquez sur "Suivant".**
![2-8](/assets/1-Création%20de%20Machines%20Virtuelles/2-8.png)

**Sélectionnez si vous souhaitez fournir une ISO maintenant ou ultérieurement.**
![2-9](/assets/1-Création%20de%20Machines%20Virtuelles/2-9.png)

**Voici le résumé de votre machine virtuelle**
**Cliquez sur "Terminer".**
![2-10](/assets/1-Création%20de%20Machines%20Virtuelles/2-10.png)

**Pour modifier le nombre de processeur virtuel, cliquez sur "Paramètre", puis dans l'onglet Processeur vous pouvez modifier le nombre de processeurs virtuels**
![2-11](/assets/1-Création%20de%20Machines%20Virtuelles/2-12.png)

**Dans notre cas nous en avons dédiés 2**

**Vous pouvez également modifier la quantité de mémoire RAM, Ajouter un matériel (Disque, Carte réseau, CD, etc..)**
![2-12](/assets/1-Création%20de%20Machines%20Virtuelles/2-11.png)
**Vous pouvez ensuite démarrer la VM, dans notre cas l'ISO était renseigné donc notre machine démarre sur le disque d'installation de WS2016.**
![2-13](/assets/1-Création%20de%20Machines%20Virtuelles/2-13.png)
**Vous pouvez ensuite choisir votre version de Windows Server 2016, nous prenons "Experience utilisateur"**
![2-14](/assets/1-Création%20de%20Machines%20Virtuelles/2-14.png)
**Vous pouvez ensuite choisir votre disque d'installation, nous prenons le disque 0**
![2-15](/assets/1-Création%20de%20Machines%20Virtuelles/2-15.png)
**La version de Windows Server 2016 s'installe"**
![2-16](/assets/1-Création%20de%20Machines%20Virtuelles/2-16.png)
**Après avoir définis vos identifiants vous arriverez-ici et votre machine est prête à l'emploie.**
![2-17](/assets/1-Création%20de%20Machines%20Virtuelles/2-17.png)

# Gestion des Machines Virtuelles
## Différence entre arrêter et mettre en pause une VM..

**Arrêter une VM** :  Arrêter une VM libère l'ensemble des ressources qu'elle utilise, comme la mémoire RAM et le(s) processeur(s) attribués. Après un arrêt, la VM doit redémarrer complètement pour être réutilisée, ce qui implique le rechargement du système d'exploitation et de toutes les applications & services.

**Mettre en pause une VM** : Suspendre une VM met temporairement toutes les activités de la VM en pause, en conservant son état actuel en mémoire ( à chaud ). Cela signifie que la mémoire RAM utilisée par la VM est toujours allouée et ne devient pas disponible pour d'autres processus. Lorsque la VM est reprise, elle continue à fonctionner exactement à partir du même point où elle a été mise en pause, sans avoir besoin de redémarrer l'ensemble du système d'exploitation.

## Quels paramètres peuvent être modifiés en cours d'exécution ?
### Lorsque la VM est en cours d'éxecution :
#### **Matériel :**
#### Microprogramme : 
- On peux modifier l'ordre de démarrage des entrées (Lecteur CD, Réseau, Disque dur)
#### Sécurité : 
- Non modifiable
#### Mémoire : 
- On peux ajuster la mémoire RAM (2048, 4096..)
- Changer la priorisation de la mémoire ( Bas, haut, etc..)
#### Processeur : 
##### On ne peux pas ajouter : 
- Des processeurs virtuels
##### On peux modifier :
- La réserve de l'ordinateur virtuel
- La limite de l'ordinateur virtuel ( pourcentage )
#### Contrôleur ISCI :
- Un lecteur CD
- Un disque dur
- Lecteur partagé
#### Carte réseau : 
- On peux changer de carte réseau, ou l'enlever
- Activer l'identification de LAN virtuelle
- Activer la gestion de bande passante
#### Gestion :
##### Nom :
- On peux modifier le nom de la machine
- Ajouter une description
##### Service d'intégration : 
- Activer / désactiver les services Hyper-V de la machine virtuelle
#### Point de contrôle :
- Activer les points de contrôle ou les modidier leur modes
- Changer l'emplacement du fichier de point de contrôle
- Emplacement du fichier de pagination intelligente : 
- On ne peux pas modifier le dossier de stockage virtuel
#### Action de démarrage automatique : 
- On peux modifier l'action de la machine virtuel lorqu'elle est stopé inopément (Arrêt de l'Hyper-V après coupure, etc..)
#### Action d'arrêt automatique : 
- On ne peux pas modifier

## Clonez une machine virtuelle existante.
**Ouvrez le "Gestionnaire Hyper-V" puis faites un clic-droit sur la VM que vous souhaitez cloner et faite *"Exporter"*.**
![3-1](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-1.png)

**Choisissez le chemin de destination pour l'exportation, nous le ferons sur le bureau dans notre cas**
![3-2](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-2.png)
![3-3](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-3.png)

**Vous pouvez voir un message dans *"Statut"* indiquant la progression de l'export**
![3-4](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-4.png)

**Une fois l'export terminé, vous pouvez voir le dossier de l'exportation sur votre bureau**
![3-5](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-5.png)

**Vous pouvez maintenant importer cette machine virtuelle**
**En haut a droite, dans les "Actions" de l'Hyper-V, cliquez sur *"Importer un ordinateur virtuel"***
**Pensez à renommer votre ancienne machine virtuelle pour éviter les conflits de nom**
![3-6](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-6.png)

**Faites *"Parcourir"* puis selectionnez le nom de dossier nommé du nom de votre VM, dans notre cas "DC3-AD-WP1"**
![3-7](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-7.png)
![3-8](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-8.png)

**Hyper-V vous confirme avoir trouvé un état de machine virtuelle à importer.**
![3-9](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-9.png)

**Faites *"Copier l'ordinateur virtuel (Créer un ID unique)"*, cela vous éviteras des conflit de SID plus tard, car réutiliser le même ID voudrait dire que nous possédons deux machines avec la même identité.**
![3-10](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-10.png)
![3-11](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-11.png)

**Cliquez sur *"Importer"*.**
**Hyper-V vous confirme que l'importation est terminée une fois réalisé.**
![3-12](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-12.png)
**Vous pouvez maintenant voir votre nouvelle machine virtuelle dans la liste des VM.**
![3-13](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-13.png)

**Vous pouvez ensuite la démarrer pour vérifier son fonctionnement**
![3-14](/assets/Gestion%20des%20Machines%20Virtuelles/Clonage%20VM/3-14.png)

## Exportez une machine virtuelle vers un autre emplacement.

### Activer la migration dynamique (Entre hyper-v)
*La migration dynamique nous permet de déplacer une VM entre deux Hyper-V dans le meme domaine, et sur le(s) même(s) réseau(x)*

**Pré-requis :**
- *Les deux serveurs doivent être dans le même domaine*

**Ouvrez le "Gestionnaire Hyper-V" puis faites un clic-droit sur le serveur Hyper-V et faite *"Paramètres Hyper-V"*.**
![4-1](/assets/Gestion%20des%20Machines%20Virtuelles/Activer%20la%20migration%20dynamique/4-1.png)

**Allez dans l'encart, *"Migration dynamique"*.**
**Cliquez sur le bouton *"Activer la migration dynamique"* et *"Utilisez n'importe quel réseau disponible pour la migration dynamique"* puis faites Appliquer.**
![4-2](/assets/Gestion%20des%20Machines%20Virtuelles/Activer%20la%20migration%20dynamique/4-2.png)
![4-3](/assets/Gestion%20des%20Machines%20Virtuelles/Activer%20la%20migration%20dynamique/4-3.png)

## Déplacer une VM avec la migration dynamique

**Ouvrez le "Gestionnaire Hyper-V" puis faites un clic-droit sur la VM que vous souhaitez déplacer et faite *"Déplacer"*.**
![5-1](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-1.png)

**Selectionnez *"Déplacer l'ordinateur virtuel"**.*
![5-2](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-2.png)

**Faites *"Parcourir"* et sélectionner l'Hyper-V vers lequel vous souhaitez migrer la VM.**
**Cliquez sur *"Suivant"*.**
![5-3](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-3.png)

**Selectionnez le type de migration que vous souhaitez effectuer.**
![5-4](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-4.png)

**Sur l'Hyper-V distant, sélectionnez l'emplacement ou la VM va être stocké en cliquant sur *"Parcourir"*.**
**Cliquez sur *"Suivant"*.**
![5-5](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-5.png)

**Une fois que le résumé vous semble correct, cliquez sur *"Terminer"*.**
![5-6](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-6.png)

**La VM va être déplacée.**
![5-7](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-7.png)

**Rendez-vous sur votre autre Hyper-v et vous pourrez constater que votre VM à été déplacée.**
![5-8](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-8.png)
![5-9](/assets/Gestion%20des%20Machines%20Virtuelles/Déplacer%20une%20VM%20avec%20la%20migration%20dynamique/5-9.png)

# Snapshots et Sauvegardes
## Créez un snapshot de la machine virtuelle.

**Ouvrez le *"Gestionnaire Hyper-V"* puis faites un clic-droit sur la VM pour lequel vous souhaitez faire un snapshot et faite *"Point de contrôle"*.**
![6-1](/assets/Gestion%20des%20Machines%20Virtuelles/Créez%20un%20snapshot%20de%20la%20machine%20virtuelle/6-1.png)
**Le point de contrôle s'effectue, vous pouvez le voir dans l'espace *"Point de contrôle"***
![6-2](/assets/Gestion%20des%20Machines%20Virtuelles/Créez%20un%20snapshot%20de%20la%20machine%20virtuelle/6-2.png)

# Revenez à un état précédent en utilisant le snapshot
**Ouvrez le *"Gestionnaire Hyper-V"* puis faites un clic-gauche sur la VM pour lequel vous souhaitez revenir à un état précédent et regardez l'onglet *"Point de contrôle"*.**
**Vous pouvez faire un clic-gauche sur un point de contrôle existant et faire *"Appliquer"* pour revenir à l'état précédent du point de contrôle.**
![7-1](/assets/Gestion%20des%20Machines%20Virtuelles/Revenez%20à%20un%20état%20précédent%20en%20utilisant%20le%20snapshot/7-1.png)
![7-2](/assets/Gestion%20des%20Machines%20Virtuelles/Revenez%20à%20un%20état%20précédent%20en%20utilisant%20le%20snapshot/7-2.png)

**La restauration s'effectue, observable dans l'onglet *"Statut"***
![7-3](/assets/Gestion%20des%20Machines%20Virtuelles/Revenez%20à%20un%20état%20précédent%20en%20utilisant%20le%20snapshot/7-3.png)

# Configurez une tâche de sauvegarde pour la machine virtuelle.

**Dans le Gestionnaire de serveur, retournez à nouveaux dans la fonction d'ajout de rôle & fonctionnalités et allez jusqu'à l'onglet *"Fonctionnalités"*, dans la liste cochez *"Sauvegardes Windows Server"*.**
![8-1](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-1.png)
![8-2](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-2.png)

**Ouvrez ensuite *"Windows Server Backup".**
![8-3](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-3.png)

**En haut à gauche, cliquez sur *"Planification de sauvegarde"*.**
![8-4](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-4.png)

**Cliquez sur *"Personnalisé"*.**
![8-5](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-5.png)

**Sélectionnez la VM que vous souhaitez sauvegarder.**
![8-6](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-6.png)

**Dans notre cas nous allons sauvegarder la VM sur un dossier partagé se situant sur notre autre Hyperviseur, afin de pouvoir la restaurer sur celui-ci en cas de corruption de notre Hyperviseur principal.**
**Nous cochons donc *"Sauvegarde sur un dossier réseau partagé"**
![8-7](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-7.png)

**Nous allons ensuite sélectionner le dossier partagé sur notre autre Hyperviseur.**
![8-8](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-8.png)

**Résumé de notre action.**
![8-9](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-9.png)

**La sauvegarde planifiée est configurée.**
![8-10](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-10.png)
![8-11](/assets/Gestion%20des%20Machines%20Virtuelles/Configurez%20une%20tâche%20de%20sauvegarde%20pour%20la%20machine%20virtuelle/8-11.png)

# Réseau Virtuel
## Configurez un commutateur virtuel
### Ajouter un réseau sur VMWARE
Nous allons ajouter le réseau *"192.168.50.0"*.
![9-1](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Ajouter%20un%20réseau%20sur%20VMWARE/9-1.png)
![9-2](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Ajouter%20un%20réseau%20sur%20VMWARE/9-2.png)
![9-3](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Ajouter%20un%20réseau%20sur%20VMWARE/9-3.png)


### Attacher un réseau via un commutateur virtuell a l'HyperV
**Maintenant que le réseau est crée, nous allons l'attacher via un nouveau commutateur virtuel *"Virtual Switch 2"*.**
![10-1](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20un%20réseau%20a%20l'HyperV/10-1.png)
![10-2](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20un%20réseau%20a%20l'HyperV/10-2.png)
![10-3](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20un%20réseau%20a%20l'HyperV/10-3.png)

## Attachez la machine virtuelle à différents réseaux virtuels.
**Retourner sur l'interface *"Gestionnaire Hyper-V"*, faites un clic-droit sur la VM sur laquel vous souhaitez attacher une nouvelle carte réseaux et cliquez sur *"Paramètre"*.**
![11-1](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20une%20carte%20réseau%20a%20la%20VM/11-1.png)

**Cliquer sur *"Ajouter un appareil"* et selectionner *"Carte réseau"*.**
![11-2](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20une%20carte%20réseau%20a%20la%20VM/11-2.png)

**Cliquer sur *"Ajouter"*.**
![11-3](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20une%20carte%20réseau%20a%20la%20VM/11-3.png)

**Selectionner le commutateur virtuel que vous souhaitez utiliser puis cliquez sur *"Appliquer"*.**
![11-4](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20une%20carte%20réseau%20a%20la%20VM/11-4.png)

## Testez la connectivité
**Vous pouvez voir que la carte réseau a bien été ajoutée.**

![11-5](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Attacher%20une%20carte%20réseau%20a%20la%20VM/11-5.png)

**On effectue un ping depuis un autre VM vers cette VM.**
![12-1](/assets/Gestion%20des%20Machines%20Virtuelles/Partie%20réseau/Testez%20la%20connectivité/12-1.png)

## Surveillance et Gestion à Distance

### Utilisez Hyper-V Manager pour surveiller les ressources de la machine virtuelle
**On peux surveiller les métriques sur l'interface en temps réel, pour pousser la gestion on peux utiliser des outils comme [PRTG](https://www.paessler.com/fr/network_monitoring_tool).**
![12-1](/assets/Gestion%20des%20Machines%20Virtuelles/Surveillance%20et%20Gestion%20à%20Distance/Utilisez%20Hyper-V%20Manager%20pour%20surveiller%20les%20ressources%20de%20la%20machine%20virtuelle/13-1.png)

## Configurez l'accès à distance à Hyper-V Manager à partir d'un autre ordinateur ou Hyper-V.

**Sur l'ordinateur distant, ouvrez le "Gestionnaire Hyper-V" puis faites un clic-droit sur *"Gestionnaire Hyper-V"* et cliquez sur *"Se connecter au serveur"*.**
![13-1](/assets/Gestion%20des%20Machines%20Virtuelles/Surveillance%20et%20Gestion%20à%20Distance/Se%20connecter%20à%20distance%20a%20Hyper-V/13-1.png)

**Nos deux Hyperviseur sont dans un domaine, donc nous pouvons selectionner l'autre Hyperviseur dans la liste des ordinateurs disponibles**
![13-2](/assets/Gestion%20des%20Machines%20Virtuelles/Surveillance%20et%20Gestion%20à%20Distance/Se%20connecter%20à%20distance%20a%20Hyper-V/13-2.png)
![13-3](/assets/Gestion%20des%20Machines%20Virtuelles/Surveillance%20et%20Gestion%20à%20Distance/Se%20connecter%20à%20distance%20a%20Hyper-V/13-3.png)
![13-4](/assets/Gestion%20des%20Machines%20Virtuelles/Surveillance%20et%20Gestion%20à%20Distance/Se%20connecter%20à%20distance%20a%20Hyper-V/13-4.png)

**Vous pouvez désormais gérer vos deux Hyperviseur dont 1 à distance sur votre Gestionnaire Hyper-V**
![13-5](/assets/Gestion%20des%20Machines%20Virtuelles/Surveillance%20et%20Gestion%20à%20Distance/Se%20connecter%20à%20distance%20a%20Hyper-V/13-5.png)
