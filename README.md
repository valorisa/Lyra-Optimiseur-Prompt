# Lyra Optimiseur Prompt

Lyra Optimiseur Prompt est un méta-prompt en français destiné à transformer
des demandes vagues en prompts clairs, structurés et directement exploitables
par un assistant d’intelligence artificielle.

Le projet applique une méthode en quatre étapes :

1. Déconstruire la demande.
2. Diagnostiquer les ambiguïtés et les informations manquantes.
3. Développer une structure adaptée au besoin.
4. Délivrer un prompt final prêt à copier-coller.

## Objectifs

Le projet vise à :

- améliorer la précision des demandes adressées aux assistants IA ;
- réduire les échanges inutiles de clarification ;
- adapter les prompts aux besoins techniques, créatifs et pédagogiques ;
- fournir une méthode réutilisable sans installation ;
- conserver un fonctionnement simple, lisible et transparent.

## Utilisation rapide

Aucune installation n'est nécessaire.

1. Ouvrir une nouvelle conversation avec un assistant IA.
2. Copier le contenu de [`lyra-prompt.md`](lyra-prompt.md).
3. Coller le contenu dans la conversation.
4. Décrire son besoin avec ses propres mots.
5. Répondre aux questions de clarification.
6. Copier le prompt optimisé dans l'assistant cible.

## Exemple

Demande initiale :

> Je veux automatiser la compilation de mon noyau WSL2.

Après clarification, Lyra peut produire un prompt précisant :

- la version du noyau ;
- l'environnement de compilation ;
- la cible matérielle ;
- les contraintes de dépendances ;
- le format des artefacts ;
- les tests attendus ;
- le workflow GitHub Actions souhaité.

## Fichiers principaux

| Fichier | Description |
| --- | --- |
| `lyra-prompt.md` | Méta-prompt principal de Lyra. |
| `.markdownlint-cli2.jsonc` | Configuration du contrôle Markdown. |
| `.github/workflows/markdownlint.yml` | Workflow de validation automatique. |
| `LICENSE` | Licence MIT du projet. |

## Validation locale

Le projet utilise `markdownlint-cli2` via `npx` :

```sh
npx --yes markdownlint-cli2 "**/*.md"
```

Pour vérifier uniquement le fichier principal :

```sh
npx --yes markdownlint-cli2 README.md
```

## Principes

Lyra :

- ne prétend pas améliorer les capacités intrinsèques du modèle ;
- ne doit pas inventer les informations manquantes ;
- pose uniquement les questions nécessaires ;
- distingue les demandes simples des demandes complexes ;
- produit un prompt final indépendant et réutilisable ;
- explique brièvement les améliorations apportées.

## Limites

La qualité du résultat dépend :

- de la précision des informations fournies ;
- des capacités de l'assistant utilisé ;
- de la vérification humaine des réponses ;
- de la qualité des contraintes et critères de réussite.

Lyra ne remplace ni l'expertise métier ni la validation technique.

## Contribution

Les contributions sont les bienvenues.

Avant de proposer une modification :

1. vérifier la syntaxe Markdown ;
2. exécuter le contrôle `markdownlint` ;
3. décrire clairement l'objectif de la modification ;
4. conserver une documentation en français.

## Licence

Ce projet est distribué sous licence MIT. Voir le fichier
[`LICENSE`](LICENSE).
