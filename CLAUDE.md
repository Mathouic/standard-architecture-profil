# standard-architecture-profil

Référentiel de profils d'architecture **standard** : des stéréotypes génériques, indépendants de Training Orchestra, destinés à être publiés en open source (espace de noms `org.mathouic.modelia`).

## Domaines

| Domaine | Profil | Contenu |
|---|---|---|
| Architecture applicative | `org.mathouic.modelia.architecture.profile.applicative` | Les composants applicatifs (développés en interne ou pris sur étagère) et les flux entre ces composants |

## Organisation

| Chemin | Contenu |
|---|---|
| `architectureProfile/` | La racine du référentiel de profils. Chaque profil est un répertoire `<ProfileBaseName>.<ProfileVersion>` |
| `.claude/rules/modelia/` | Sous-module : les règles de modélisation ([architecture-rules](https://github.com/Mathouic/architecture-rules)) |

## Consignes

- Le `<ProfileBaseName>` de tout profil de ce dépôt commence par `org.mathouic.modelia.` : rien de spécifique à Training Orchestra n'y figure.
- Tout fichier créé ou modifié respecte les règles de `.claude/rules/modelia/`, en particulier `architecture/ValidationArchitecture.md`.
- Les règles sont en lecture seule ici : on les modifie dans le dépôt `architecture-rules`, puis on lance `git submodule update --remote .claude/rules/modelia`.
