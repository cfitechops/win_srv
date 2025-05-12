# Partage de fichiers Windows : NTFS ou partagé, comment attribuer des autorisations de dossier

#### Objectifs :

- Comprendre l'importance du partage de fichiers dans un environnement en réseau
- Apprenez à partager efficacement des fichiers et des dossiers
- Faites la différence entre les types de partage de réseau et leurs cas d’utilisation.
- Comprendre comment les autorisations contrôlent l'accès des utilisateurs aux fichiers partagés
- Apprenez à accéder efficacement aux dossiers partagés

#### Autorisations NTFS et autorisations de partage

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

- Voici le dossier marketing ce que nous voulons faire les autorisations, cliquez droit sur le dossier que vous souhaitez vérifier et que cliquez sur propriétés et cliquez sur l'onglet de partage.

![NTFS](/05_NTFS/assets/01.png)

- Ajoutons les autorisations de partage pas le NTFS donc si nous cliquons sur les autorisations

![NTFS](/05_NTFS/assets/02.png)

- Nous verrons les différents types d'autorisations de partage que vous pouvez donner à différents utilisateurs ou groupes donc comme vous pouvez le voir, il n'y a que vous êtes contrôle total des autorisations.

![NTFS](/05_NTFS/assets/03.png)

- Vérifications les autorisations ncfs. Les autorisations ncfs peuvent être trouvées dans l'onglet sécurité et comme vous pouvez le voir,il ya plus d'autorisations par rapport au partage précédent. Il y a un contrôle total, modifier la lecture et exécuter, cliquez simplement sur modifier.

![NTFS](/05_NTFS/assets/04.png)

- Et ensuite nous pouvons ajouter

![NTFS](/05_NTFS/assets/05.png)

- Il suffit de rechercher leur nom de groupe, cela dépend de votre entreprise.

![NTFS](/05_NTFS/assets/06.png)

- Un stagiaire en marketing doit accéder au dossier partagé de l'équipe `marketing` Marketingpour afficher le contenu, mais ne doit pas modifier ni supprimer de fichiers.

![NTFS](/05_NTFS/assets/07.png)

![NTFS](/05_NTFS/assets/08.png)

#### Activité 2 : Activité pratique

- Le service RH a besoin d'un dossier sécurisé, HRGroup, accessible uniquement aux employés des RH. Les autres employés ne doivent pas le voir.

> Faisons clic droit sur le dossier; allons dans les propriétés et clics sur l'onglet partage et partage avancé, cliquons sur partager ce dossier

![NTFS](/05_NTFS/assets/09.png)

![NTFS](/05_NTFS/assets/10.png)

> Cliquer sur supprimer car nous ne voulons pas que quiconque à quelqu'un d'autre que les RH voie ce dossier, puis ajoutons le, puis modifions leur autorisation en contrôle total puisque nous voulons que les RH aient uniquement accès.

![NTFS](/05_NTFS/assets/11.png)

![NTFS](/05_NTFS/assets/12.png)

![NTFS](/05_NTFS/assets/13.png)

![NTFS](/05_NTFS/assets/14.png)

- Cliquez sur l'onglet sécurité, comme vous pouvez le voir le groupe RH est le département RH n'est pas encore ajouté et nouq clics sur l'utilisateur, nous pouvons voir qu'ils n'ont que les autorisations de lecture et d'exécution et de lecture du contenu du dossier de liste.

- Cliquez sur edit et ajouter à cela également, ajoutons RH groupe et nous pouvons leur donner le contrôle total au niveau NTFS également, assurez-vous simplement que si vous modifiez quelque chose sur l'autorisation de partage, vérifiez également si l'autorisation ncfs doit être modifiée ou modifiée également. Ils devraient être autorisés à faire tout ce qui se trouve dans leurs dossiers.

![NTFS](/05_NTFS/assets/15.png)

![NTFS](/05_NTFS/assets/16.png)

![NTFS](/05_NTFS/assets/17.png)

![NTFS](/05_NTFS/assets/18.png)

![NTFS](/05_NTFS/assets/19.png)

#### Activité 3 : Activité pratique

- Un fournisseur tiers a besoin d'accéder à un dossier temporaire `VendorFiles` pour télécharger des rapports, mais ne doit pas voir d'autres fichiers.

> Faisons clic droit dessus et cliquons sur Propriétés, allons donc aux autorisations partagées, cliquons sur partage et partage avancé, puis autorisations et il est déjà partagé avec tout le monde, mais il n'a qu'un accès en lecture, alors ajoutons le fournisseurs et recherchons son groupe, donnons-leur le contrôle total sur ces autorisations partagées parce que nous voulons qu'ils puissent télécharger et accéder aux autres fichiers sous ce dossier

![NTFS](/05_NTFS/assets/20.png)

![NTFS](/05_NTFS/assets/21.png)

![NTFS](/05_NTFS/assets/22.png)

![NTFS](/05_NTFS/assets/23.png)

![NTFS](/05_NTFS/assets/24.png)

- Autorisation NTFS et voyons quelle autorisation nous pouvons donner au fournisseur et la seule tâche que nous voulons que le fournisseur fasse est de télécharger des rapports afin qu'il ne voie pas les autres fichiers sous le nom de fournisseur et tout ce qu'il a à faire est de télécharger car il pourrait y avoir d'autres fichiers qu'il n'est pas autorisé à voir ou à lire car ils pourraient être confidentiels. Nous devons donc restreindre cette autorisation afin que le fournisseur ne puisse effectuer qu'une seule tâche qui est le téléchargement.

![NTFS](/05_NTFS/assets/25.png)

![NTFS](/05_NTFS/assets/26.png)

![NTFS](/05_NTFS/assets/27.png)

![NTFS](/05_NTFS/assets/28.png)

![NTFS](/05_NTFS/assets/29.png)

#### Activité 4 : Activité pratique

- Au sein du département informatique, tous les techniciens doivent avoir accès au référentiel de logiciels, mais seul le personnel informatique senior doit pouvoir accéder au `Licences` sous-dossier.

- Faisons clic droit dessus et cliquons sur Propriétés, allons donc aux autorisations partagées, cliquons sur partage et partage avancé, puis autorisations

![NTFS](/05_NTFS/assets/30.png)

![NTFS](/05_NTFS/assets/31.png)

![NTFS](/05_NTFS/assets/32.png)

![NTFS](/05_NTFS/assets/33.png)

![NTFS](/05_NTFS/assets/34.png)

- Il est indiqué dans l'activité que seul le personnel informatique `senior` devrait pouvoir accéder au sous-dossier des licences, donc ajustons l'autorisation de ces sous-dossiers pour autoriser uniquement l'accès à l'informatique `senior`.

![NTFS](/05_NTFS/assets/35.png)

![NTFS](/05_NTFS/assets/36.png)

![NTFS](/05_NTFS/assets/37.png)

![NTFS](/05_NTFS/assets/38.png)

![NTFS](/05_NTFS/assets/39.png)

![NTFS](/05_NTFS/assets/40.png)

![NTFS](/05_NTFS/assets/41.png)

![NTFS](/05_NTFS/assets/42.png)

#### Question bonus

- Si un utilisateur dispose d'autorisations de lecture sur un dossier NTFS mais d'un contrôle total sur le partage, quelle est son autorisation effective lors de l'accès au dossier sur le réseau ?
