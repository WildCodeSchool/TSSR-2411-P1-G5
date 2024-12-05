# Guide Utilisateur v2.57.1 de KeePass2

## Sommaire

[Nous allons créer une nouvelle base de données dans KeePass2](#nous-allons-créer-une-nouvelle-base-de-données-dans-keepass2)

[Ajouter un mot de passe](#ajouter-un-mot-de-passe)

[Utiliser les mots de passe enregistrés](#utiliser-les-mots-de-passes-enregistrés)

[Modifier ou récupérer des informations d'une entrée](#modifier-ou-récupérer-des-informations-dune-entrée)

[Modifier la séquence Auto-Type](#modifier-la-séquence-auto-type)

[FAQ - Keepass](#faq---keepass)



## Nous allons créer une nouvelle base de données dans KeePass2

### **Préparer la base de données**
- Ouvrez le menu "Fichier" et sélectionnez "Nouveau". Puis, cliquez sur "OK" dans la fenêtre qui s'affiche et confirmez la création d'une nouvelle base de données.

![Capture d'écran 2024-12-04 120203](https://github.com/user-attachments/assets/4360b292-5ea0-4675-a0b6-d07c2485d628)

- Choisir l'emplacement du fichier
  
Sélectionnez le dossier où vous souhaitez stocker le fichier .kdbx.

![Capture d'écran 2024-12-04 120432](https://github.com/user-attachments/assets/acd1709e-688e-4708-9097-cbe68198f548)

- Définir le MasterPassword
Ensuite, vous devrez définir un mot de passe principal, appelé "MasterPassword", qui permet d'accéder à la plateforme où vos mots de passe sont sauvegardés. Ce mot de passe doit être à la fois complexe et suffisamment facile à mémoriser.

![Capture d'écran 2024-12-04 120714](https://github.com/user-attachments/assets/034b1072-5a4a-44f3-b329-5ee50dd1e2d5)

Pour créer un mot de passe robuste, il est recommandé d'utiliser une passphrase, un mot de passe composé de plusieurs caractères. On parle de passphrase car elle ressemble parfois à une phrase pour des raisons de mémorisation.

![Capture d'écran 2024-12-04 120714](https://github.com/user-attachments/assets/ac31e32f-93e5-450d-824f-cdd9a9c7d723)

- Activer les options avancées
Cochez "Afficher les options de l'Expert". Vous aurez la possibilité d'améliorer la sécurité de la base de données en ajoutant un fichier clé, que vous pouvez créer en cochant "Ajouter un fichier clé" et en cliquant sur "Créer".
Ce fichier clé contient une clé cryptée et ne doit pas être modifié, car toute modification vous empêcherait d'accéder à votre base de données. Il sert à réaliser une authentification à deux facteurs, renforçant ainsi la sécurité (le mot de passe principal + le fichier clé).

![Capture d'écran 2024-12-04 120904](https://github.com/user-attachments/assets/eae624ce-49aa-4f6d-b68c-5af393276d7a)

- Créer le fichier clé
Vous aurez le choix entre deux formats de clé :

Version 2.0 : La nouvelle version compatible avec KeePass2 (à choisir).

Version 1.0 : Une ancienne version compatible avec des versions plus anciennes de KeePass et les versions portables (à éviter dans ce cas).

![Capture d'écran 2024-12-04 121002](https://github.com/user-attachments/assets/5496a916-2953-4cdc-9cae-b3bdb34cc92d)

Sélectionnez le format "2.0 (recommandé)" pour continuer. Vous pourrez alors créer une clé en deux étapes :

À la souris : Déplacez votre curseur de manière aléatoire sur le carré à gauche pour générer une clé de sécurité robuste.

Au clavier : Tapez des chaînes de caractères aléatoires pour générer la clé.
Nommer et décrire la base de données

![Capture d'écran 2024-12-04 121037](https://github.com/user-attachments/assets/4ed595bd-92f8-4796-8236-252eb354c8ac)

Une fois la clé générée, donnez un nom à votre base de données et, si vous le souhaitez, ajoutez une description.

![Capture d'écran 2024-12-04 121223](https://github.com/user-attachments/assets/34108546-8c91-4c03-a066-1fadeed98d7f)

Imprimer une copie de sécurité
- KeePass propose une option pour imprimer un formulaire qui contient vos informations de sécurité. 
Vous pouvez le remplir manuellement et le conserver dans un endroit sûr. 

- Cliquez sur "Imprimer" ou "Passer" si vous préférez ignorer cette étape.

![Capture d'écran 2024-12-04 121339](https://github.com/user-attachments/assets/beafbd61-db97-4bb1-8eba-617605a92497)

Ajouter des mots de passe dans KeePass

- Création des groupes
Votre base de données est maintenant prête à accueillir vos mots de passe. KeePass organise les informations en différents groupes comme "Général", "Windows", "Réseau", "Internet", "Courriel", et "Banque à domicile". Vous pouvez aussi créer de nouveaux groupes personnalisés.

## **Ajouter un mot de passe**
Pour ajouter, par exemple, les identifiants de votre compte Facebook, sélectionnez le groupe "Internet", puis déroulez le menu "Entrée" et choisissez "Ajouter une entrée" (ou utilisez le raccourci Ctrl + I).

![Capture d'écran 2024-12-04 121418](https://github.com/user-attachments/assets/f4aefa6c-cbae-4969-b808-f7f854dac060)

- Saisie des informations
Dans la fenêtre qui apparaît, indiquez le "Titre" que vous souhaitez attribuer à l'entrée. Ensuite, saisissez votre identifiant, votre mot de passe, et l'URL du site. 

Cliquez sur "OK" ou utilisez le raccourci Ctrl + S pour enregistrer l'entrée.

![Capture d'écran 2024-12-04 121633](https://github.com/user-attachments/assets/4abaa804-358d-4b74-97e8-95663831c714)

## Utiliser les mots de passe enregistrés

- Ouvrir la base de données
Ouvrez KeePass avec la base de données contenant vos informations personnelles. Une fois ouverte, vous devrez rechercher l'entrée contenant le mot de passe souhaité.

- Rechercher une entrée
Utilisez le raccourci Ctrl+F ou cliquez sur l'onglet "Find" puis "Find" pour lancer la recherche. Dans le champ "Find what", tapez simplement le nom recherché (site web, nom d'utilisateur, etc.). Les résultats s'afficheront en fonction des informations présentes dans vos entrées.

![Capture d'écran 2024-12-04 121928](https://github.com/user-attachments/assets/0c386ef1-cfd5-4787-8d91-bae7d62b4ed1)


- Ouvrir un site
Une fois l'entrée trouvée, faites un clic droit dessus, puis sélectionnez "URL(s)" > "Open with ..." pour ouvrir le site associé dans votre navigateur.

![Capture d'écran 2024-12-04 122453](https://github.com/user-attachments/assets/a0604e5f-5854-4a69-ab25-361a32153c26)


Saisie automatique
Pour remplir automatiquement votre identifiant et mot de passe, placez le curseur sur le champ de connexion du site et appuyez sur Ctrl + V. KeePass saisira alors automatiquement vos informations de connexion.

- Afficher ou copier un mot de passe
Si vous souhaitez voir un mot de passe, faites un clic droit sur l'entrée, sélectionnez "Edit", puis cliquez sur l'icône `...` à côté du mot de passe pour l'afficher.
Vous pouvez aussi copier le mot de passe en le sélectionnant et en faisant un clic droit sur "Copier".

![Capture d'écran 2024-12-04 122713](https://github.com/user-attachments/assets/084bc34c-d1d7-4a30-bdfd-5a3fa8cacf96)


## **Modifier ou récupérer des informations d'une entrée**

- Accéder aux informations
Pour récupérer des informations détaillées sur une entrée, faites un clic droit sur l'entrée désirée et sélectionnez "Edit entry". Vous aurez alors accès à toutes les informations liées à cette entrée (identifiant, mot de passe, URL, etc.).

![Capture d'écran 2024-12-04 122802](https://github.com/user-attachments/assets/4cc9c31e-b77f-49e3-a004-a96d68573176)




## **Modifier la séquence Auto-Type**
- Configurer l'Auto-Type pour une saisie automatique réussie
Pour garantir que l'auto-type fonctionne correctement, vous devrez peut-être modifier la commande "exécuter" et remplacer par une séquence personnalisée.
Faites un clic droit sur l'entrée, sélectionnez "Edit entry", puis allez dans l'onglet "Auto-Type".

![Capture d'écran 2024-12-04 122908](https://github.com/user-attachments/assets/e6c02b17-5b73-43ae-8978-d404e9b7670d)

 - Cochez "Override default sequence" pour personnaliser la séquence.

![Capture d'écran 2024-12-04 123007](https://github.com/user-attachments/assets/6a3336fc-b64d-4f03-bc16-86d539e733e7)

- Voici quelques séquences possibles :

{USERNAME}{TAB}{PASSWORD}{ENTER} : Séquence par défaut pour les sites où le login et le mot de passe se trouvent sur la même page, séparés par un onglet.
{USERNAME}{ENTER}{DELAY 1500}{PASSWORD}{ENTER} : Séquence pour les sites avec une connexion en deux étapes (par exemple, Amazon).
{USERNAME}{TAB}{TAB}{PASSWORD}{ENTER} : Séquence pour les sites où le login et le mot de passe sont sur la même page, mais avec un onglet séparant les deux champs (par exemple, La Poste).





## FAQ - Keepass

1. ## J'ai oublié mon mot de passe principal, que faire ?
Si vous avez oublié votre mot de passe principal, il n'est pas possible de le récupérer. KeePass crypte la base de données avec ce mot de passe, donc sans lui, vous ne pouvez pas accéder à vos données. Il est crucial de conserver ce mot de passe en lieu sûr.

2. ## Comment synchroniser ma base de données sur plusieurs appareils ?
Pour utiliser KeePass sur plusieurs appareils, enregistrez votre fichier .kdbx dans un service de stockage en ligne comme Google Drive, Dropbox ou OneDrive. Vous pourrez alors accéder à votre fichier depuis n'importe quel appareil tout en garantissant que vous avez toujours la dernière version.

3. ## Que faire si mon fichier de base de données est corrompu ?
Si votre fichier .kdbx est corrompu, KeePass ne pourra pas le réparer. Il est recommandé d'avoir des sauvegardes régulières de votre fichier pour pouvoir le restaurer en cas de problème.

4. ## Comment utiliser les clés de fichiers pour renforcer la sécurité ?
Vous pouvez ajouter une clé de fichier pour renforcer la sécurité de votre base de données. Lors de la création de votre base, sélectionnez l'option "Charger une clé de fichier" et conservez cette clé en sécurité. Elle est nécessaire pour déverrouiller votre base de données en complément du mot de passe.

5. ## Comment organiser mes mots de passe dans KeePass ?
Dans KeePass, vous pouvez organiser vos mots de passe en groupes. Pour cela, créez des groupes comme "Travail", "Banques", ou "Personnel" pour mieux gérer vos mots de passe et retrouver rapidement ceux dont vous avez besoin.

6. ## Puis-je partager des mots de passe en toute sécurité ?
Oui, vous pouvez partager votre base de données KeePass avec d'autres utilisateurs, à condition qu'ils aient accès au mot de passe principal ou à la clé de fichier. Assurez-vous d'utiliser des moyens sécurisés pour partager le fichier .kdbx, comme le chiffrement, pour éviter tout risque.

7. ## Recommandations supplémentaires :
Sauvegardes régulières : N'oubliez pas de sauvegarder régulièrement votre fichier KeePass pour éviter la perte de données en cas de corruption ou de suppression accidentelle.
Double sécurité avec la clé de fichier : Utilisez la clé de fichier en plus du mot de passe principal pour une sécurité renforcée, surtout si vos mots de passe sont sensibles.
