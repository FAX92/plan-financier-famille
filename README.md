# Plan de match financier, jeune famille Québec 2026

Outil web interactif et gratuit pour bâtir le plan de match financier d’une jeune famille au Québec : budget réel, congé parental (RQAP), allocations, comptes enregistrés (CELI, REER, CELIAPP, REEE), dettes, protection et succession, projet immobilier, projections et plan d’action. Quand toutes les questions requises sont répondues, l’outil produit un PDF complet, directement dans le navigateur.

Site : `https://<votre-compte>.github.io/<nom-du-depot>/`

## Ce que fait l’outil

- Dix étapes guidées, sauvegardées automatiquement sur l’appareil (aucun serveur, aucune collecte).
- Estimations en direct : revenu net 2026 (impôt fédéral et québécois, RRQ, assurance-emploi, RQAP), prestations RQAP selon le régime choisi, Allocation canadienne pour enfants et Allocation famille, patrimoine net, test de résistance hypothécaire, droits de mutation, comparaison location et achat, projections à trois scénarios.
- Tableau de bord : indicateurs, feux (fonds d’urgence, taux d’épargne, logement, dettes, coussin du congé, REEE, protection juridique, test de résistance) et priorités classées selon les réponses.
- PDF d’une douzaine de pages : sommaire exécutif, famille et congé, budget, bilan et dettes, fiscalité et ordre de priorité des cotisations, immobilier, projections, protection et cadre juridique québécois (union parentale, testament, tuteur), feuille de route de 12 mois, hypothèses et sources, mandat de révision pour Claude.
- Paramètres 2026 modifiables (plafonds, taux, seuils) et réinitialisables.
- Exportation et importation des réponses en JSON, bouton pour copier un mandat d’analyse avec les données.

## Confidentialité

Tout se passe dans le navigateur. Les réponses sont enregistrées dans le stockage local de l’appareil et le PDF est produit localement. La page ne contient aucune donnée personnelle : la version publique part vide. Le PDF, lui, contient les renseignements saisis : retirer les informations sensibles avant de le transmettre à un service externe.

## Mise en ligne sur GitHub Pages

1. Créer un dépôt public sur GitHub (par exemple `plan-financier-famille`).
2. Téléverser les fichiers `index.html`, `manifest.json`, `icon-192.png`, `icon-512.png` et `README.md` à la racine du dépôt (bouton « Add file », puis « Upload files », puis « Commit changes »).
3. Dans le dépôt : Settings, puis Pages. Sous « Build and deployment », choisir Source : « Deploy from a branch », Branch : `main`, dossier `/ (root)`, puis Save.
4. Attendre une à deux minutes. L’adresse publique s’affiche dans la section Pages : `https://<votre-compte>.github.io/<nom-du-depot>/`.
5. Sur iPhone : ouvrir l’adresse dans Safari, Partager, puis « Sur l’écran d’accueil » pour l’installer comme une application.

Pour mettre à jour : téléverser de nouveau `index.html` avec le même nom (GitHub remplace l’ancien fichier), puis attendre la reconstruction de la page. Si l’ancienne version s’affiche encore, recharger sans cache.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | L’application complète (HTML, CSS, JavaScript, générateur PDF) |
| `manifest.json` | Manifeste web pour l’installation sur l’écran d’accueil |
| `icon-192.png`, `icon-512.png` | Icônes de l’application |
| `README.md` | Ce guide |

Dépendance externe : la bibliothèque pdfmake (version 0.2.21) est chargée depuis cdnjs.cloudflare.com au chargement de la page. Les polices Manrope et JetBrains Mono sont chargées depuis Google Fonts avec repli sur les polices système.

## Paramètres 2026 et sources

Valeurs vérifiées en octobre 2026 : CELI 7 000 $ (109 000 $ cumulés), REER 33 810 $, CELIAPP 8 000 $ par année et 40 000 $ à vie, RAP 60 000 $, SCEE 20 % et IQEE 10 % sur 2 500 $, RQAP revenu maximal assurable 103 000 $ et cotisation 0,430 %, RRQ 6,30 % (MGA 74 600 $, MSGA 85 000 $), assurance-emploi 1,30 % (68 900 $), paliers fédéraux (14 % à 33 %) et québécois (14 % à 25,75 %, indexation 2,05 %), ACE 8 157 $ et 6 883 $ (seuils 38 237 $ et 82 847 $), Allocation famille 3 068 $ max et 1 221 $ min, droits de mutation 0,5 % jusqu’à 62 900 $, 1 % jusqu’à 315 000 $, 1,5 % au-delà, contribution réduite en garderie 9,65 $ par jour.

Sources : canada.ca (ARC), revenuquebec.ca, retraitequebec.gouv.qc.ca, rqap.gouv.qc.ca, quebec.ca, Loi concernant les droits sur les mutations immobilières, SCHL et BSIF. Les valeurs changent chaque année : les vérifier à la date d’utilisation et les ajuster dans « Paramètres 2026 ».

## Avertissement

Cet outil fournit de l’information générale et des estimations. Il ne constitue pas un conseil financier, fiscal ou juridique et ne remplace pas un planificateur financier, un fiscaliste, un courtier d’assurance ou un notaire.

## Licence

MIT. Libre d’utilisation, de modification et de redistribution, sans garantie.
