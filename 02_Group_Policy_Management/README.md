# Gestion des stratégies de groupe

- Group Policy Object (GPO), signifie objet de stratégie de group.
- GPO est donc un ensemble de strategies et d'Active Directory qui peuvent être appliqués aux domaines et aux O us.
- Les GPO sont donc utilisés par les administrateurs pour gérer les paramètres aux utilisateurs et aux ordinateurs.

#### Activité 1 : Politique relative aux mots de passe

- Définissez une politique de mot de passe pour appliquer des mots de passe forts et améliorer la sécurité.

> Allons dans votre machine et tapez `Group Policy Management > Domains > srv22.local > Create a GPO in this domain, and Link it here...`.

> Nous allons donc nommer cela la strategie de mot de passe.

![GPO](/02_Group_Policy_Management/assets/04.png)

> Faites un clic droit sur cette stratégie de mot de passe et cliquez sur modifier.

![GPO](/02_Group_Policy_Management/assets/05.png)

![GPO](/02_Group_Policy_Management/assets/06.png)

#### Activité 2 : Cartographie des lecteurs

- Mappez les lecteurs réseau pour les utilisateurs lorsqu'ils se connectent

> Allons dans votre machine et tapez `Group Policy Management > Domains > srv22.local > Create a GPO in this domain, and Link it here...`.

> Creons un GPO, puis nommons-le Drive Mapping, et lorsque vous faites un clic droit dessus, cliquez simplement sur modifier

![GPO](/02_Group_Policy_Management/assets/08.png)

> `Drive Mapping > User Configuration > Preferences > Windows Settings > Drive Maps > New > Mapped Drive`

![GPO](/02_Group_Policy_Management/assets/09.png)

![GPO](/02_Group_Policy_Management/assets/10.png)

![GPO](/02_Group_Policy_Management/assets/11.png)

#### Activité 3 : Politique relative aux fonds d'écran

- Définissez un fond d’écran de bureau par défaut pour tous les utilisateurs.

> Clic droit sur votre domaine créons un GPO.

![GPO](/02_Group_Policy_Management/assets/12.png)

> Puis cliquez sur modifer.

![GPO](/02_Group_Policy_Management/assets/13.png)

> `Desktop Wallpaper > User Configuration > Policies > Administrative Templates Policy definitions > Desktop > Desktop`

![GPO](/02_Group_Policy_Management/assets/14.png)

![GPO](/02_Group_Policy_Management/assets/15.png)

#### Activité 4 : Restreindre l'accès au panneau de configuration

- Empêcher les utilisateurs d’accéder au panneau de configuration.

> Créons le GPO, clic sur le domaine et créez un GPO nommons le restreindre le panneau de configurations.

![GPO](/02_Group_Policy_Management/assets/16.png)

> Puis modifions

![GPO](/02_Group_Policy_Management/assets/17.png)

> `Restrict Control Panel > User Configuration > Policies > Administrative Templates Policy definitions > Control Panel`

![GPO](/02_Group_Policy_Management/assets/18.png)

![GPO](/02_Group_Policy_Management/assets/19.png)

![GPO](/02_Group_Policy_Management/assets/20.png)

![GPO](/02_Group_Policy_Management/assets/18.png)

![GPO](/02_Group_Policy_Management/assets/19.png)

![GPO](/02_Group_Policy_Management/assets/20.png)

#### Activité 5 : Désactiver le stockage USB

- Empêcher les utilisateurs d’utiliser des périphériques de stockage USB.

> Créons le GPO, clic sur le domaine et créez un GPO nommons le périphérique USB.

![GPO](/02_Group_Policy_Management/assets/21.png)

![GPO](/02_Group_Policy_Management/assets/22.png)

![GPO](/02_Group_Policy_Management/assets/23.png)

![GPO](/02_Group_Policy_Management/assets/24.png)

![GPO](/02_Group_Policy_Management/assets/25.png)

![GPO](/02_Group_Policy_Management/assets/26.png)

#### Bonus : Politique de verrouillage de compte

- Configurez les paramètres de verrouillage de compte pour empêcher les attaques par force brute.
