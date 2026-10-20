# standard-architecture-profil

Référentiel de profils d'architecture **standard** : des stéréotypes génériques, indépendants de Training Orchestra, destinés à être publiés en open source (espace de noms `org.mathouic.modelia`).

## Domaines

Les profils sont rangés dans un référentiel par notion de la [typologie des components](.claude/rules/modelia/Definitions.md#typologie-des-components) et, pour les contextes et les composants applicatifs, par famille. Chaque famille `<Famille>` a deux profils : `org.mathouic.modelia.architecture.profile.<Famille>.applicationcontext` (les contextes applicatifs, dans `applicativeContext/`) et `org.mathouic.modelia.architecture.profile.<Famille>.applicative` (les composants applicatifs qu'ils hébergent, dans `applicativeComponent/`).

La notion reste dans le nom du profil, même si le référentiel la porte déjà : un modèle ne déclare pas deux profils de même `<ProfileBaseName>` (règle `M-05`), et il peut utiliser les profils `data` des deux référentiels à la fois.

| Famille | Contextes applicatifs | Composants applicatifs |
|---|---|---|
| `runtime` | IIS, site IIS, .NET Framework, .NET, Kestrel, service Windows, Node.js | Application web, API web, worker |
| `data` | SQL Server, Azure SQL, PostgreSQL, Redis, compte de stockage Azure, SSIS, SSRS | Base de données, schéma, conteneur blob, partage de fichiers, package SSIS, rapport SSRS |
| `identity` | Keycloak, tenant Entra ID, domaine Active Directory, ADFS | Royaume, client OIDC, inscription d'application, application d'entreprise, partie de confiance |
| `azure` | App Service, Function App, API Management, Logic App, Key Vault, App Configuration | Fonction, API managée, workflow, secret, certificat |
| `messaging` | Azure Service Bus, RabbitMQ, Azure Event Grid, Kafka | File, topic, abonnement, exchange |
| `observability` | Application Insights, Log Analytics, Seq, Elasticsearch, Grafana | Tableau de bord |
| `client` | Navigateur web, Office, Teams, OS mobile | SPA, complément Office, application Teams, application mobile |

| Profil | Contenu |
|---|---|
| `org.mathouic.modelia.architecture.profile.system` (dans `system/`) | Les composants systèmes : l'infrastructure sur laquelle s'exécutent les contextes applicatifs (machine virtuelle, conteneur, Kubernetes…) et le réseau (réseau virtuel, load balancer, pare-feu…) |
| `org.mathouic.modelia.architecture.profile.applicative` (dans `applicativeComponent/`) | Les stéréotypes applicatifs transverses, hors famille (vide pour l'instant) |

Les icônes `_100` suivent un style par notion : pictogramme bleu pour un composant applicatif, carré bleu pour un contexte applicatif, carré gris ardoise pour un composant système.

## Organisation

| Chemin | Contenu |
|---|---|
| `applicativeComponent/` | Le référentiel des profils de composants applicatifs |
| `applicativeContext/` | Le référentiel des profils de contextes applicatifs |
| `system/` | Le référentiel des profils de composants systèmes |
| `Stereotypes.md` | Le catalogue des stéréotypes, par référentiel puis par famille |
| `.claude/rules/modelia/` | Sous-module : les règles de modélisation ([architecture-rules](https://github.com/Mathouic/architecture-rules)) |
| `.claude/settings.json` | Active le plugin `modelia-claude-plugin` : les skills partagés ([modelia-claude-plugin](https://github.com/Mathouic/modelia-claude-plugin)) |

Chaque référentiel a un `metainfo.yaml` racine (`type: architecture.profiles`). Chaque profil y est un répertoire `<ProfileBaseName>.<ProfileVersion>`.

## Consignes

- Le `<ProfileBaseName>` de tout profil de ce dépôt commence par `org.mathouic.modelia.` : rien de spécifique à Training Orchestra n'y figure.
- Un stéréotype va dans le profil de sa notion (composant applicatif, contexte applicatif ou composant système) et de sa famille. Un hôte liste les components qu'il héberge dans `innerComponents` (composant système → contexte applicatif → composant applicatif).
- Tout ajout, retrait ou modification d'un stéréotype (méta-informations, icône) est reporté dans `Stereotypes.md`, avec une description courte.
- Tout fichier créé ou modifié respecte les règles de `.claude/rules/modelia/`, en particulier `architecture/ValidationArchitecture.md`.
- Les règles sont en lecture seule ici : on les modifie dans le dépôt `architecture-rules`, puis on lance `git submodule update --remote .claude/rules/modelia`.
