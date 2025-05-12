# Services de fichiers Configuration du partage réseau sur Windows Server

- Configurer le partage de fichiers dans l’environnement AD.

#### Objectives:

- Acquérir une expérience pratique avec AD et les services de partage de fichiers.
- Pratiquez la configuration et la gestion des ressources et des autorisations du réseau.

> **Partage réseau**

> **Types d'autorisation**

> **Gestionnaire de ressources du service de fichiers**

```sh
Permissions and Access Control ->   Read  |  Write  |  Execute  |  Full Control

-----------------------------------------------------------------------

Types of Permissions ->    NTFS    |    Share

-----------------------------------------------------------------------

Sharing Methods ->   Mapped  |  Network
```

![File Services](/03_File_Services/assets/00.png)

#### Activité 1 : Configurer un partage de fichiers

- Configurer le partage de fichiers
  > Créez des dossiers partagés avec les autorisations appropriées. Définissez les autorisations NTFS et de partage
  > pour permettre l'accès aux utilisateurs du domaine.

![File Services](/03_File_Services/assets/01.png)

![File Services](/03_File_Services/assets/02.png)

![File Services](/03_File_Services/assets/03.png)

![File Services](/03_File_Services/assets/04.png)

![File Services](/03_File_Services/assets/05.png)

#### Activité 2 : Configuration des machines clientes

- Accéder aux ressources partagées

  > Connectez-vous aux machines clientes à l'aide de comptes d'utilisateur de domaine. Mappez les lecteurs

  > Réseau pour accéder aux dossiers partagés.

- Ouvrez l'explorateur de fichiers et faites un clic droit sur le PC et selectionnez `Mapper le lecteur réseau`.

![File Services](/03_File_Services/assets/06.png)

![File Services](/03_File_Services/assets/07.png)

![File Services](/03_File_Services/assets/08.png)

```sh
Sharing Methods ->  Network  |  Mapped
```

#### Activité 3 : Configuration des GPO

- Configurez les objets de stratégie de groupe (GPO) pour mapper automatiquement les lecteurs réseau pour les utilisateurs.

![File Services](/03_File_Services/assets/09.png)

![File Services](/03_File_Services/assets/10.png)

![File Services](/03_File_Services/assets/11.png)

![File Services](/03_File_Services/assets/12.png)

![File Services](/03_File_Services/assets/13.png)

![File Services](/03_File_Services/assets/14.png)

#### Activité 4 : Mettre en œuvre des quotas et un filtrage des fichiers à l'aide du gestionnaire de ressources du serveur de fichiers (FSRM)

- Configurez FSRM pour créer un modèle de quota et un modèle d'écran de fichiers afin de gérer efficacement le stockage de fichiers dans votre organisation.

![File Services](/03_File_Services/assets/15.png)

![File Services](/03_File_Services/assets/16.png)

![File Services](/03_File_Services/assets/17.png)

![File Services](/03_File_Services/assets/18.png)

![File Services](/03_File_Services/assets/19.png)

- Développons cela et de même avec Quotas il y a un paramètre différent, donc la gestion du filtrage des fichiers consiste essentiellement à contrôler les types de fichiers que vous pouvez autoriser sur ce dossier partagé. Donc les exemples de types de fichiers sont (`.DOC , .JPG , .PNG , .EPS , .CDR , .TXT , .GIF, .MP3 , .WAV , .AI , .MOV , .EXE , .DMG , .RAR , .ZIP , .PDF`)

![File Services](/03_File_Services/assets/20.png)

![File Services](/03_File_Services/assets/21.png)

![File Services](/03_File_Services/assets/22.png)

![File Services](/03_File_Services/assets/23.png)

![File Services](/03_File_Services/assets/24.png)
