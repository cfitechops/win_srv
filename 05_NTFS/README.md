# Partage de fichiers Windows : NTFS ou partagé, comment attribuer des autorisations de dossier

#### Objectives:

- Undestand the importance of file sharing in a networked environement
- Learn how to share files and folders effectively
- Differentiate between network sharing types and their use cases.
- Undestand how permissions control user access to shared files
- Learn how to access hared folders efficiently

#### NTFS vs Share Permissions

```sh
------------------|------------------------------------------------|---------------------------------------------|
Features          |        NTFS Permissions                        | Share Permissions                           |
------------------|------------------------------------------------|---------------------------------------------|
Where it Applies  |   Local & network users (on the file system)   | Network users (accessing via shared folder) |
------------------|------------------------------------------------|---------------------------------------------|
Granular Control  |   Very detailed (Full Control, Modify,         | Full Control, Change, Read                  |
                  |   Read & Execute, etc.)                        |                                             |
------------------|------------------------------------------------|---------------------------------------------|
```

- Voici le dossier marketing ce que nous voulons faire les autorisations, clic droit sur le dossier que vous souhaitez verifier et que cliquez sur propriétés et cliquez sur l'onglet de partage.

![NTFS](/05_NTFS/assets/01.png)

- Ajoutons les autorisations de partage pas le NTFS donc si nous cliquons sur les autorisations

![NTFS](/05_NTFS/assets/02.png)

- Nous verrons les differents types d'autorisations de partage que vous pouvez donner à différents utilisateurs ou groupes donc comme vous pouvez le voir, il n'y a que tois autorisations control total

![NTFS](/05_NTFS/assets/03.png)

- Vérifions les autorisations ncfs. Les autorisations ncfs peuvent être trouvées dans l'onglet sécurité et comme vous pouvez le voir,il ya plus d'autorisations par rapport au partage précédent. Il ya un contrôle total, modifier la lecture et éxecuter, cliquez simplement sur modifier

![NTFS](/05_NTFS/assets/04.png)

- Et ensuite nous pouvons ajouter

![NTFS](/05_NTFS/assets/05.png)

- Il suffit de rechercher leur nom de groupe, cela depend de votre entreprise.

![NTFS](/05_NTFS/assets/06.png)

- A marketing intern needs access to the Marketing Team's shared folder `Marketing` to view content but should not modify or delete files.

![NTFS](/05_NTFS/assets/07.png)

![NTFS](/05_NTFS/assets/08.png)

#### Activity 2: Hands-on activity

- The HR Department needs a secure folder HRGroup that only HR staff can access. Other employees should not see the folder at all.

> Faisons clic droit sur le dossier; allons dans les propriétés et cliquons sur l'onglet partage et partage avancé, cliquons sur partager ce dossier

![NTFS](/05_NTFS/assets/09.png)

![NTFS](/05_NTFS/assets/10.png)

> Cliquer sur supprimer car nous ne voulons pas que quiconque à quelqu'un d'autre que les RH voie ce dossier, puis ajoutons le, puis modifions leur autorisation en contrôle total puisque nous voulons que les RH aient uniquement accès.

![NTFS](/05_NTFS/assets/11.png)

![NTFS](/05_NTFS/assets/12.png)

![NTFS](/05_NTFS/assets/13.png)

![NTFS](/05_NTFS/assets/14.png)

> Cliquer sur l'onglet sécurité, comme vous pouvez le voir le groupe RH est le département RH n'est pas encore ajouté et nouq cliquons sur l'utilisateur, nous pouvons voir qu'ils n'ont que les autorisations de lecture et d'exécution et de lecture du contenu du dossier de liste.

> Cliquer sur edit et ajouter à cela également, ajoutons RH groupe et nous pouvons leur donner le contrôle total au niveau NTFS également, assurez-vous simplement que si vous modifiez quelque chose sur l'autorisation de partage, verifiez également si l'autorisation ncfs doit être ajustée ou modifiée également. Ils devraient être autorisés a faire tout ce qui se trouve dans leurs dossiers.

![NTFS](/05_NTFS/assets/15.png)

![NTFS](/05_NTFS/assets/16.png)

![NTFS](/05_NTFS/assets/17.png)

![NTFS](/05_NTFS/assets/18.png)

![NTFS](/05_NTFS/assets/19.png)

#### Activity 3: Hands-on activity

- A third-party vendor needs access to a temporary folder **VendorFiles** to upload reports but should not see other files.

> Faisons clic droit dessus et cliquons sur Propriétés, allons donc aux autorisations partagées, cliquons sur partage et partage avancé, puis autorisations et il est déjà partagé avec tout le monde, mais il n'a qu'un accès en lecture, alors ajoutons le fourniseur et recherchons son groupe, donnons-leur le contrôle total sur ces autorisations partagées parceque nous voulons qu'ils puissent télécharger et accéder aux autres fichiers sous ce dossier partagé.

![NTFS](/05_NTFS/assets/20.png)

![NTFS](/05_NTFS/assets/21.png)

![NTFS](/05_NTFS/assets/22.png)

![NTFS](/05_NTFS/assets/23.png)

![NTFS](/05_NTFS/assets/24.png)

- Autorisation NTFS et voyons quelle autorisation nous pouvons donner au fournisseur et la seule tâche que nous voulons que le fournisseur fasse est de télécharger des rapports afin qu'il ne voie pas les autres fichiers sous le nom de fournisseur et tout ce qu'il a à faire est de télécharger car il pourrait y avoir d'autres fichiers qu'il n'est pas autorisé à voir ou à lire car ils pourraient être confidentiels. Nous devons donc restreindre cette autorisation afin que le fournisseur ne puisse effectuer q'une seule tâche qui est le telechargement.

![NTFS](/05_NTFS/assets/25.png)

![NTFS](/05_NTFS/assets/26.png)

![NTFS](/05_NTFS/assets/27.png)

![NTFS](/05_NTFS/assets/28.png)

![NTFS](/05_NTFS/assets/29.png)

#### Activity 4: Hands-on activity

- In the IT Department, all techs need access to the Software Repository **Software** but only senior IT staff should be able to access the `Licences` subfolder.

> Faisons clic droit dessus et cliquons sur Propriétés, allons donc aux autorisations partagées, cliquons sur partage et partage avancé, puis autorisations

![NTFS](/05_NTFS/assets/30.png)

![NTFS](/05_NTFS/assets/31.png)

![NTFS](/05_NTFS/assets/32.png)

![NTFS](/05_NTFS/assets/33.png)

![NTFS](/05_NTFS/assets/34.png)

- Il est indiqué dans l'activité que seul le personnel informatique senior devrait pouvoir accéder au sous-dossier des licences, donc ajustons l'autorisation de ces sous-dossiers pour autoriser uniquement l'accès à l'informatique senior.

![NTFS](/05_NTFS/assets/35.png)

![NTFS](/05_NTFS/assets/36.png)

![NTFS](/05_NTFS/assets/37.png)

![NTFS](/05_NTFS/assets/38.png)

![NTFS](/05_NTFS/assets/39.png)

![NTFS](/05_NTFS/assets/40.png)

![NTFS](/05_NTFS/assets/41.png)

![NTFS](/05_NTFS/assets/42.png)

#### Bonus Question

- If a user has read permissions on an NTFS folder but Full control on the share, what is their effective permission when accessing the folder over the network ?
