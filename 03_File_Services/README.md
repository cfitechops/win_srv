# File Services Setting up Network Sharing on Windows Server

- Set up file sharing within the AD environment.

#### Objectives:

- Gain pratical experience with AD, file sharing services.
- Pratice setting up and managing network resources and permissions.

> **Network Sharing**

> **Permission Types**

> **File Service Resource Manager**

```sh
Permissions and Access Control ->   Read  |  Write  |  Execute  |  Full Control

-----------------------------------------------------------------------

Types of Permissions ->    NTFS    |    Share

-----------------------------------------------------------------------

Sharing Methods ->   Mapped  |  Network
```

![File Services](/03_File_Services/assets/00.png)

#### Activity 1: Set Up a File Sharing

- Configure File Sharing
  > Create shared folders with appropriate permissions.
  > Set NTFS and share permissions to allow domain users access.

![File Services](/03_File_Services/assets/01.png)

![File Services](/03_File_Services/assets/02.png)

![File Services](/03_File_Services/assets/03.png)

![File Services](/03_File_Services/assets/04.png)

![File Services](/03_File_Services/assets/05.png)

#### Activity 2: Set Up Client Machines

- Access Shared Resources

  > Log in to the client machines using domain user accounts.
  > Map network drives to access shared folders.

- Ouvrez l'explorateur de fichiers et faites un clic droit sur le PC et selectionnez `Mapper le lecteur réseau`.

![File Services](/03_File_Services/assets/06.png)

![File Services](/03_File_Services/assets/07.png)

![File Services](/03_File_Services/assets/08.png)

```sh
Sharing Methods ->  Network  |  Mapped
```

#### Activity 3: GPO Configuration

- Configure Group Policy Objects (GPOs) to automatically map network drives for users.

![File Services](/03_File_Services/assets/09.png)

![File Services](/03_File_Services/assets/10.png)

![File Services](/03_File_Services/assets/11.png)

![File Services](/03_File_Services/assets/12.png)

![File Services](/03_File_Services/assets/13.png)

![File Services](/03_File_Services/assets/14.png)

#### Activity 4: Implement quotas and file screening using File Server Resource Manager (FSRM)

- Configure FSRMto create Quota Template and File Screen Template to effectively manage File Storage in your organization

![File Services](/03_File_Services/assets/15.png)

![File Services](/03_File_Services/assets/16.png)

![File Services](/03_File_Services/assets/17.png)

![File Services](/03_File_Services/assets/18.png)

![File Services](/03_File_Services/assets/19.png)

- Développons cela et de même avec Quotas il ya un paramètre différent, donc la gestion du filtrage des fichiers consiste essentiellement à contrôler les types de fichiers que vous pouvez autoriser sur ce dossier partagé. Donc les exemples de types de fichiers sont (`.DOC , .JPG , .PNG , .EPS , .CDR , .TXT , .GIF, .MP3 , .WAV , .AI , .MOV , .EXE , .DMG , .RAR , .ZIP , .PDF`)

![File Services](/03_File_Services/assets/20.png)

![File Services](/03_File_Services/assets/21.png)

![File Services](/03_File_Services/assets/22.png)

![File Services](/03_File_Services/assets/23.png)

![File Services](/03_File_Services/assets/24.png)
