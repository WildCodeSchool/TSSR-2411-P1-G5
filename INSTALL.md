1ère partie : installation windows serveur


![Capture d'écran 2024-12-05 105734](https://github.com/user-attachments/assets/065e510a-e210-4189-bc5e-339534b47bc8)

2ème partie : installatiion keepass sur windows serveur

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
