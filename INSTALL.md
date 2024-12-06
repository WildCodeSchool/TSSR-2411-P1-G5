
Ce document présente la procédure d'installation de Windows Server 2022, Ubuntu et Keepass. Certaines étapes sont expliquées de manière détaillée pour prendre en compte les différentes spécificités des installations et configurations.

# SOMMAIRE 

- [1ère partie : étapes d'installation et Configuration de Windows Server 2022](1ère-partie-:-étapes-d'installation-et-Configuration-de-Windows-Server-2022)
- [2ème partie : Guide d'installation v2.57.1 de KeePass2](2ème-partie-:-guide-d'installation-v2.57.1-de-KeePass2)
- [3ème partie : installation keepass sur ubuntu](3ème-partie-:-installation-keepass-sur-ubuntu)
  
## 1ère partie : étapes d'installation et Configuration de Windows Server 2022

### Configuration VM (VirtualBox)

- Sur votre VM, cliquer sur Nouvelle;
- Nommer la machine SRVWIN01;
  
![Capture d'écran 2024-12-05 115712](https://github.com/user-attachments/assets/a0801cfb-d1f1-4e95-acaa-b2296685a710)


- Ajouter l'ISO Windows server 2022 téléchargeé préalablement sur internet pour l'ajouter par la suite dans la partie "ISO Image";


![Capture d'écran 2024-12-05 115904](https://github.com/user-attachments/assets/37564f55-50ac-4086-87c6-a819f23364df)


- Aller dans l'onglet "Hardware";
- Ajouter au minimun 2 à 4 Go de RAM et 2 CPU;


![Capture d'écran 2024-12-05 110516](https://github.com/user-attachments/assets/5f27bf23-eac3-4beb-a44b-735a90fbb138)

- Aller dans l'onglet "Hard Disk";
- Choisir l'espace de stockage que l'on souhaite attribuer à la machine (conseillé : 40 Go);

![Capture d'écran 2024-12-05 120009](https://github.com/user-attachments/assets/c0a46ca6-b531-4626-a4a1-47e1c3997fd4)

- Démarrer le Windows Server 2022;

![Capture d'écran 2024-12-05 110700](https://github.com/user-attachments/assets/c9fb5a00-d0ee-4700-b295-2d8b70cc10b6)

- Au début de l'installation, vous pouvez choisir la langue que vous souhaitez pour l'installation;
-  Choisir "French" pour le "Time and currency format";
-  Choisir "French" pour avoir le configuration du clavier en Français;
  
![Capture d'écran 2024-12-05 110739](https://github.com/user-attachments/assets/116bb49b-ae52-4c91-aad6-34b5601c7317)

- Pour le système d'exploitation à installer, il est conseillé de sélectionner la version Standard avec Expérience utilisateur (*Standard Evaluation (Desktop Experience)*) car nous avons besoin d'une interface graphique et nous ne sommes pas sur un projet de Datacenter;
- Cliquer sur "Next";
- Cocher pour accepter les termes du contrat de license puis cliquer sur "Next";

![Capture d'écran 2024-12-05 110815](https://github.com/user-attachments/assets/84eebfb5-f85e-4191-9b2f-fb7d3afcee37)

- Choisir l'installation "Custom";
- Garder la configuration par défaut;
- Cliquer sur "Next";

![Capture d'écran 2024-12-05 110921](https://github.com/user-attachments/assets/cf714a24-14b0-4fb3-8871-523e7b443f6b)

- Laisser le système s'installer;
- Une fois le système installé, il est demandé de choisir un nom d'utilisateur qui sera "Administrateur" et un mot de passe qui sera "Azerty01";

![Capture d'écran 2024-12-05 110946](https://github.com/user-attachments/assets/c46debe3-df3d-4c05-836e-9236214f1bb6)

- Cliquer sur "Yes" pour confirmer la découverte de la machine par d'autres machines du réseau;

![Capture d'écran 2024-12-05 111017](https://github.com/user-attachments/assets/1b382da2-2af2-43c4-be89-676a7c972c6f)

- Rentrer votre mot de passe et accéder à votre session;
- Aller dans le "Gestionnaire de Service" s'il ne s'ouvre pas automatiquement;

![Capture d'écran 2024-12-05 111248](https://github.com/user-attachments/assets/b8bc37d7-8888-4659-8324-09a5df4f9627)

- Aller dans "Serveur local";
- Cliquer sur l'adresse Ethernet;
- Clique droit sur "Ethernet" et "Propriétés";

![Capture d'écran 2024-12-05 112754](https://github.com/user-attachments/assets/04169614-59a1-4390-aa9e-169d43859826)

- Un onglet "Gestion de réseau" apparaît;
- Cliquer sur "Protocole Internet version 4" puis sur "Prorpiétés";
- Aller dans "Configuration alternative" puis rentrer l'adresse IP et le masque de sous-réseau (255.255.255.0);
- Appuyer sur "Ok" pour valider les changements;

![Capture d'écran 2024-12-05 112852](https://github.com/user-attachments/assets/b23c1145-bacc-4ddf-8d97-a390a7e83565)

- Dans le gestionnaire de réseau puis serveur local, cliquer sur Pare-feu Microsoft Defender;
- Cliquer sur désactiver pour "réseau avec domaine", "Réseau privé", "Réseau public" puis retourner dans le gestionnaire de serveur;
  
![Capture d'écran 2024-12-05 113014](https://github.com/user-attachments/assets/f69e6686-6cf7-4068-a791-8c5313c268cb)

- Pour pouvoir partager nos documents, il est important d'installer le "NFS";
- Pour cela, aller dans "Gérer" puis "Ajouter des rôles et des fonctionnalités";
- Dans "Installation type", sélectionner "Installation basée surun rôle ou une fonctionnalité" puis cliquer sur "Suivant";
- Vérifier si le serveur cible est correct puis cliquer sur "Suivant";
  
![Capture d'écran 2024-12-05 113504](https://github.com/user-attachments/assets/d652bb3f-87f7-44e3-9721-4ef656dc0576)

- Dans "Rôles de serveurs", développer "Services de fichiers et de stockage" puis "Services de fichiers et iSCSI";
- Selectionner "Serveur pour NFS" puis "Suivant";

![Capture d'écran 2024-12-05 113613](https://github.com/user-attachments/assets/9c22ea78-704b-4f46-a83f-df3473420941)

- Cliquer sur "Ajouter des fonctionnalités" puis "Suivant";
- Dans "Fonctionnalités" cliquer sur "Suivant";
- Cliquer sur "Installer" sur l'onglet de confirmation pour débuter l'installation;
- Cliquer sur "Fermer" une fois l'installation terminé;

![Capture d'écran 2024-12-05 114259](https://github.com/user-attachments/assets/1727abe1-8635-44f7-8a93-7fa0dc4b1277)

- Une fois ces étapes faites, aller dans le dossier KeePass créé préalablement et qui contient la BDD (voir le USER_GUIDE.md pour créer une nouvelle base de donnée);
- Une fois sur le dossier, clique droit sur le dossier puis "Propriété", puis "Partagé",
- Noter le chemin du réseau qui sera utilisé par la suite pour le client;
- Cliquer sur "Paratgé"; 

![Capture d'écran 2024-12-05 113139](https://github.com/user-attachments/assets/b56c523e-13b7-4119-92fc-3145da72b33e)

- Sur "Tout le monde", donner les droits d'écritue et de lecture seulement;
- Votre dossier est maintenant mis en réseau et est visible par les clients;
![Capture d'écran 2024-12-05 113247](https://github.com/user-attachments/assets/d8302be2-01df-4143-a141-1384523f23d0)

Nous allons maintenant expliquer l'installation et la configuration de KeePass.



# _**Guide d'installation v2.57.1 de KeePass2**_

### Sommaire

- [Étape 1 : Télécharger KeePass 2](https://github.com/WildCodeSchool/TSSR-2411-P1-G5/blob/main/INSTALL.md#etape-1--t%C3%A9l%C3%A9charger-keepass-2)
- [Étape 2 : Lancer l'exécutable](https://github.com/WildCodeSchool/TSSR-2411-P1-G5/blob/main/INSTALL.md#%C3%A9tape-2--lancer-lex%C3%A9cutable)
- [Étape 3 : Lancer l'installation](https://github.com/WildCodeSchool/TSSR-2411-P1-G5/blob/main/INSTALL.md#%C3%A9tape-3--lancer-linstallation)
- [Étape 4 : Finaliser l'installation](https://github.com/WildCodeSchool/TSSR-2411-P1-G5/blob/main/INSTALL.md#%C3%A9tape-4--finaliser-linstallation)
- [Étape 5 : Lancer KeePass 2](https://github.com/WildCodeSchool/TSSR-2411-P1-G5/blob/main/INSTALL.md#%C3%A9tape-5--lancer-keepass-2)
- [Étape 6 : Changement de langue (optionnel)](https://github.com/WildCodeSchool/TSSR-2411-P1-G5/blob/main/INSTALL.md#%C3%A9tape-6--changement-de-langue--optionel)






##  Etape 1 : Télécharger Keepass 2
Rendez-vous sur le site officiel **[keepass](https://keepass.info/)** "À l'heure de la documentation, la version 2.57.1 est celle à télécharger."
Cliquez sur le lien intitulé "KeePass 2.57.1 Released". (Si vous ne trouvez pas la version 2.57.1, téléchargez la version la plus récente ou, lors de la première utilisation, KeePass vous proposera une mise à jour automatique.)


![Capture d'écran 2024-11-27 084802](https://github.com/user-attachments/assets/42022a5f-9a31-4923-8981-28181b652886)

Ce lien vous redirige vers la page de téléchargement, où plusieurs options de version sont proposées. Choisissez la version "Normale" (en mode installation). La version "Portable" est une version qui ne nécessite pas d'installation et peut être utilisée depuis une clé USB.

![Capture d'écran 2024-11-27 084906](https://github.com/user-attachments/assets/2bc3ab47-197e-4a49-93bf-0846037c2a84)


## Étape 2 : Lancer l'exécutable

Une fois le fichier téléchargé, cliquez sur l'exécutable pour démarrer l'installation.

![Capture d'écran 2024-11-27 085221](https://github.com/user-attachments/assets/21cc6c3f-ba79-4921-8b4f-e94da16aaa93)

## Étape 3 : Lancer l'installation

Au début de l'installation, le logiciel vous demandera de choisir la langue de l'assistant d'installation. Sélectionnez "Français" et cliquez sur "Suivant".

![Capture d'écran 2024-11-26 210830](https://github.com/user-attachments/assets/02c4dd0a-91e6-4ae8-9732-e096b65eb342)


Ensuite, l'accord de licence s'affichera, et vous devrez l'accepter pour continuer l'installation.

![Capture d'écran 2024-12-05 113001](https://github.com/user-attachments/assets/4629bfd3-64f4-4b0d-8d4c-9144fddc975c)

Dans les étapes suivantes, vous pourrez choisir le dossier d'installation. Par défaut, KeePass sera installé dans le répertoire c:\Program Files\KeePass Password Safe 2.
Si vous souhaitez installer KeePass dans un autre dossier ou sur un autre disque, cliquez sur "Parcourir" et sélectionnez le dossier de votre choix.

![Capture d'écran 2024-11-26 210906](https://github.com/user-attachments/assets/b0cb5698-42e8-4b9c-8262-3be7283f8a12)


***Lors de cette étape***, vous devrez choisir le type d'installation :

- Installation complète : installe tous les composants du logiciel.
- Installation compacte : installe uniquement les fichiers de base.
- Installation personnalisée : vous permet de sélectionner les composants spécifiques à installer.

![Capture d'écran 2024-11-26 210927](https://github.com/user-attachments/assets/ed18fe71-6bbc-4697-86c0-32eb8e31a057)

Ensuite, KeePass vous proposera d'associer le logiciel avec l'extension de fichier .kdbx (qui correspond au format de la base de données). Vous aurez aussi la possibilité d'ajouter une icône sur le bureau.

![Capture d'écran 2024-11-26 210950](https://github.com/user-attachments/assets/69be4cf7-fe93-4b4e-9e65-9f62516992f1)


## Étape 4 : Finaliser l'installation
- Cliquez sur "Installer" pour commencer l'installation avec les options que vous avez choisies.

![Capture d'écran 2024-11-26 211018](https://github.com/user-attachments/assets/bda2f763-99a6-49f2-a957-69c76f30bf6b)


## Étape 5 : Lancer KeePass 2
- Une fois l'installation terminée, vous pouvez cliquer sur "Terminer" pour lancer KeePass. Vous aurez la possibilité de choisir si vous souhaitez exécuter le logiciel immédiatement, en laissant ou non la case "Exécuter KeePass" cochée.

![Capture d'écran 2024-11-26 211040](https://github.com/user-attachments/assets/ae73a1e8-a812-48da-9cd3-ceb8055768c4)

## Étape 6 : Changement de LANGUE ( Optionel)

- Sur l'application aller sur l'onglet view puis Change Language

![Capture d'écran 2024-12-05 105329](https://github.com/user-attachments/assets/63cbfefe-2c5c-44a2-a294-d598ee275bbb)

- Puis cliquer sur Get More Languages 

![Capture d'écran 2024-12-05 105339](https://github.com/user-attachments/assets/934620c5-dc94-4142-bde8-92de284757f8)


- Une page web va s'ouvrir avec les choix de langue disponibles. Nous allons choisir le français

![Capture d'écran 2024-12-05 105142](https://github.com/user-attachments/assets/c148fe06-040b-4fc8-bac8-240631f487d6)

- Le téléchargement va se lancer automatiquement. Ensuite, vous pourrez récupérer votre fichier dans le dossier des téléchargements, comme vous l'avez fait pour le logiciel KeePass

![Capture d'écran 2024-12-05 105242](https://github.com/user-attachments/assets/e1ccdb9f-b68d-4c18-856d-a5e082c48bae)

- Allez dans le dossier où le logiciel a été installé. Ensuite, créez un dossier nommé 'Languages'.

![Capture d'écran 2024-12-05 114229](https://github.com/user-attachments/assets/641eb1a6-85c8-445b-a560-8f3e687d4775)

- Faites un copier-coller du fichier téléchargé, puis collez-le dans le dossier 'Languages'.


![Capture d'écran 2024-12-05 115502](https://github.com/user-attachments/assets/5b0d7610-0779-42bf-82df-576456f39b00)

- Démarrez le logiciel, allez dans 'View', puis Change Language et choisissez la langue de votre choix

  
 ![Capture d'écran 2024-12-05 123158](https://github.com/user-attachments/assets/03446c04-6ad9-46e0-ac2e-18c14a45231b)

- Rédemarrez le logiciel voilà c'est en Français


![Capture d'écran 2024-12-05 122740](https://github.com/user-attachments/assets/780c4002-1668-4bfb-9316-b61b4c6dd38e)

# 3ème partie : installation keepass sur ubuntu

Ouvrez un terminal et éxécuter la commande suivante pour installer keepass2:
>sudo apt install keepass2

![Capture d'écran 2024-12-04 123757](https://github.com/user-attachments/assets/d535c67b-ccc1-4bf8-8ec6-4c7cd4a83735)

Une fois l'installation terminée ouvrir keepass2. Lors du premier lancement keepass2 sera en anglais, pour changer la langues :
Allez dans *View > Change Language...* 

![Capture d'écran 2024-12-04 123840](https://github.com/user-attachments/assets/976b3c93-7bb5-4262-9f57-3f547f9d4bb3)

Une fenêtre s'affiche avec les langues disponibles. Pour ajouter d'autre languages cliquer sur *Get More languages...* 

![Capture d'écran 2024-12-04 123858](https://github.com/user-attachments/assets/b095b4f4-a4f2-40c6-ac0a-7730a80b6b92)

Une page du site officiel s'ouvre avec les fichiers de traductions disponibles. Télécharger la langue souhaitée dans notre cas le Francais en chosissant la version correspondante.

![Capture d'écran 2024-12-04 123934](https://github.com/user-attachments/assets/ca76a55a-7345-47c1-a449-5e99ab8e9384)

Une fois le fichier téléchargé, en extraire l'archive 

![Capture d'écran 2024-12-04 124019](https://github.com/user-attachments/assets/e21cd2a3-cf2a-42f7-a2fe-7e58ee971689)

Placer le fichier dans le répertoire /lib/keepass2/Languages
>sudo mv ~/Téléchargements/French.lngx /lib/keepass2/Languages/

![Capture d'écran 2024-12-04 124046](https://github.com/user-attachments/assets/b83efda3-6a27-40bb-b471-9d45ad99ca23)


![Capture d'écran 2024-12-04 124650](https://github.com/user-attachments/assets/57f54ef7-ca96-4262-ab50-3856c899c063)

Redémarrez keepass2 et selectionner la nouvelle langues ajouté

![Capture d'écran 2024-12-04 124714](https://github.com/user-attachments/assets/11343290-40a9-4d7a-8e58-0f4ef2543a0c)

Allons enfants de la Patrie, Le jour de gloire est arrivé !

![Capture d'écran 2024-12-04 124741](https://github.com/user-attachments/assets/8f0b448f-96c5-4fb9-a553-f42ef2d412bd)

Creer un dossier /mnt/keepass qui sera le répertoire où le partage réseaux sera monté et ou seront accessibles les fichiers du partage
>sudo mkdir /mnt/keepass

![Capture d'écran 2024-12-05 100840](https://github.com/user-attachments/assets/c325ab5b-e027-49da-a30d-f0df53a16dc0)

![Capture d'écran 2024-12-04 125733](https://github.com/user-attachments/assets/28b234bb-6617-4f34-ab1d-b60374488634)

![Capture d'écran 2024-12-04 130648](https://github.com/user-attachments/assets/b7a10c5e-780c-4b42-9752-6224cd44c4ff)

![Capture d'écran 2024-12-04 130619](https://github.com/user-attachments/assets/bc9e8e6b-440a-4861-8d8c-bd618e1f8ab4)
