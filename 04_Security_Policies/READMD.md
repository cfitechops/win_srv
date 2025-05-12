# Politique de sécurité

- Comprendre et mettre en œuvre les mesures de sécurité essentielles

- Mise en œuvre des politiques de sécurité | Mots de passe à granularité fine

#### Activité 1 : Configuration de la politique de mot de passe

- Configurez et appliquez une politique de mot de passe fort (12 caractères ou plus) pour les utilisateurs AD.

  > Minimum password length

  > Password Complexity
  
  > Password Age

- Clic droit sur modifier et que choisissons-nous

![Security Policy](/KEEPS/04_Security_Policies/assets/01.png)

- Sélectionner la configuration de l'ordinateur

`Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy`

![Security Policy](/KEEPS/04_Security_Policies/assets/02.png)

#### Activity 2: Account Policy Configuration

- Configure and account lockout policy to project against brute-force attacks.

  > Password threshold
  > Password lockout duration
  > The higher threshold, the higher the probability for a successful brute force attack

`Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy`

![Security Policy](/KEEPS/04_Security_Policies/assets/03.png)

> Reset Account Lockout counter after: 30 minutes

#### Activity 3: User Rights Assignment

- Assign and restrict user rights to enhance security

  > `Deny Logon Locally`

  > `Restrict Remote Desktop Access`

![Security Policy](/KEEPS/04_Security_Policies/assets/04.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/05.png)

`Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > User Rights Assignment`

> Recherchez donc Refuser la connexion locale

![Security Policy](/KEEPS/04_Security_Policies/assets/06.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/07.png)

> Puis ajoutez des groupes pour les utilisateurs qui ne doivent pas se conneter directement aux serveurs #Groupe #.

![Security Policy](/KEEPS/04_Security_Policies/assets/08.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/09.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/10.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/11.png)

#### Activity 4: Implementing Fine-Grained Password Policies

- Apply different password policies to different groups of users.
- Scenario: The organization wants to apply stricter password policies to administrative accounts while allowing standard users to have less stringent requirements.

> Open the Active Directory Administrative Center (ADAC)

> Cliquez sur votre `nom de domaine`,

> Puis sélectionnez `System > Password Settings Container`

> Créer un nouvel objet de paramètres de mot de passe ou PSO.

![Security Policy](/KEEPS/04_Security_Policies/assets/12.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/13.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/14.png)

> Définir la politique de mot de passe administrateur, puis x est la priorité. Cela détermine l'ordre dans lequel les objets de politique sont appliqués lorsque plusieurs paramètre de mot de passe sont appliqués à un utilisateur ou à un groupe.

> Par exemple, il ya un utilisateur avec deux paramètres de mot de passe, le premier paramètre avec le priorité de `20` et le deuxième avec la priorité de `30` donc celui avec le numéro le plus bas aura la présidence et c'est lui avec la présidence `20` donc pour ce paramètre de mot de passe administrateur

```sh
Setting 1 = 20
Setting 2 = 30
```

![Security Policy](/KEEPS/04_Security_Policies/assets/15.png)

![Security Policy](/KEEPS/04_Security_Policies/assets/16.png)
