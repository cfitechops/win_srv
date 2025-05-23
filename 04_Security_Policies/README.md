# Politique de sécurité

- Comprendre et mettre en œuvre les mesures de sécurité essentielles

- Mise en œuvre des politiques de sécurité | Mots de passe à granularité fine

#### Activité 1 : Configuration de la politique de mot de passe

- Configurez et appliquez une politique de mot de passe fort (12 caractères ou plus) pour les utilisateurs AD.

  > Longueur minimale du mot de passe

  > Complexité du mot de passe

  > Âge du mot de passe

- Cliquez droit sur modifier et que choisissons-nous

![Security Policy](/04_Security_Policies/assets/01.png)

- Sélectionnez la configuration de l'ordinateur

`Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy`

![Security Policy](/04_Security_Policies/assets/02.png)

#### Activité 2 : Configuration de la politique de compte

- Configurez une politique de verrouillage de compte pour vous protéger contre les attaques par force brute.

  > Seuil de mot de passe

  > Durée de verrouillage du mot de passe

  > Plus le seuil est élevé, plus la probabilité d'une attaque par force brute réussie est élevée.

`Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy`

![Security Policy](/04_Security_Policies/assets/03.png)

> Réinitialiser le compteur de verrouillage du compte après : 30 minutes

#### Activité 3 : Attribution des droits d'utilisateur

- Attribuer et restreindre les droits des utilisateurs pour améliorer la sécurité

  > `Deny Logon Locally`

  > `Restrict Remote Desktop Access`

![Security Policy](/04_Security_Policies/assets/04.png)

![Security Policy](/04_Security_Policies/assets/05.png)

`Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > User Rights Assignment`

> Recherchez donc Refuser la connexion locale

![Security Policy](/04_Security_Policies/assets/06.png)

![Security Policy](/04_Security_Policies/assets/07.png)

> Puis ajoutez des groupes pour les utilisateurs qui ne doivent pas se conneter directement aux serveurs #Groupe #.

![Security Policy](/04_Security_Policies/assets/08.png)

![Security Policy](/04_Security_Policies/assets/09.png)

![Security Policy](/04_Security_Policies/assets/10.png)

![Security Policy](/04_Security_Policies/assets/11.png)

#### Activité 4 : Mise en œuvre de politiques de mots de passe précises

- Appliquez différentes politiques de mot de passe à différents groupes d’utilisateurs.

- **Scénario** : l’organisation souhaite appliquer des politiques de mot de passe plus strictes aux comptes administratifs tout en permettant aux utilisateurs standard d’avoir des exigences moins strictes.

> Ouvrir le centre d'administration Active Directory (ADAC)

> Cliquez sur votre `nom de domaine`,

> Puis sélectionnez `System > Password Settings Container`

> Créer un nouvel objet de paramètres de mot de passe.

![Security Policy](/04_Security_Policies/assets/12.png)

![Security Policy](/04_Security_Policies/assets/13.png)

![Security Policy](/04_Security_Policies/assets/14.png)

- Définir la politique de mot de passe administrateur, puis x est la priorité. Cela détermine l'ordre dans lequel les objets de politique sont appliqués lorsque plusieurs paramètre de mot de passe sont appliqués à un utilisateur ou à un groupe.

- Par exemple, il ya un utilisateur avec deux paramètres de mot de passe, le premier paramètre avec le priorité de `20` et le deuxième avec la priorité de `30` donc celui avec le numéro le plus bas aura la présidence et c'est lui avec la présidence `20` donc pour ce paramètre de mot de passe administrateur

```sh
Setting 1 = 20
Setting 2 = 30
```

![Security Policy](/04_Security_Policies/assets/15.png)

![Security Policy](/04_Security_Policies/assets/16.png)
