# Skill `artiste-auteur` — le régime des artistes-auteurs pour les agents IA

Un skill pour Claude Code (et les agents compatibles : Codex, Cursor, etc.) qui couvre le régime social et fiscal des **artistes-auteurs** en France : écrivains, illustrateurs, photographes, compositeurs, auteurs audiovisuels, créateurs qui vivent de plateformes d'abonnement (Patreon, Substack, Ko-fi, Tipeee…).

**Lire d'abord : [DISCLAIMER.md](DISCLAIMER.md).** Ce skill est fourni en l'état, à titre informatif. Il ne remplace ni un expert-comptable, ni un avocat, ni une réponse écrite de l'URSSAF ou de la DGFiP. Chaque utilisateur reste seul responsable de ses déclarations.

## Ce que le skill sait faire

- Dire **qui relève du régime** (art. R. 382-1-1 CSS), ce qui est revenu principal et ce qui est revenu accessoire.
- Expliquer **l'affiliation** (guichet unique URSSAF artistes-auteurs), le **précompte** et la **dispense de précompte**, le cas des revenus de plateformes sans précompte.
- Calculer les **cotisations 2026** (assiette = bénéfice + 15 %, taux détaillés), la **retraite complémentaire RAAP** (IRCEC), les droits ouverts.
- Poser la **TVA** propre aux auteurs : franchises de l'art. 293 B I bis, taux de 10 %, retenue des éditeurs (285 bis).
- Traiter **l'impôt sur le revenu** : traitements et salaires ou BNC, micro-BNC, déclaration 2042 C PRO.
- Articuler le régime avec une **micro-entreprise** de formation ou de conseil.
- Chiffrer une **régularisation** de revenus non déclarés : majorations, intérêts, échéanciers, prescription.
- Signaler ce que **DAC7** change (ou pas) pour les revenus de plateformes.

Un calculateur est fourni : `scripts/calc_artiste_auteur.py`.

Toutes les valeurs sont **datées** (`data/sources.json`, en-tête de chaque fiche de `references/`) et renvoient à des **sources primaires** : Légifrance, BOFiP, urssaf.fr, secu-artistes-auteurs.fr, IRCEC, Afdas. Dernière mise à jour : 3 octobre 2026.

## Installation

### Claude Code

```bash
git clone https://github.com/DavidManise/skill-artiste-auteur ~/.claude/skills/artiste-auteur
```

Puis, dans une session Claude Code, le skill se déclenche sur les mots du domaine (artiste-auteur, droits d'auteur, précompte, URSSAF Limousin, IRCEC, RAAP, Patreon, Substack, 2042 C PRO, 5HQ, régularisation…) ou à la demande : `/artiste-auteur`.

Pour un seul projet plutôt que pour tout le compte : cloner dans `.claude/skills/artiste-auteur` à la racine du projet.

### Autres agents

Le dossier est autonome (aucun lien symbolique, aucune dépendance externe). Copier l'ensemble du dépôt dans le répertoire de skills de l'agent, en gardant `SKILL.md` à la racine du dossier `artiste-auteur/`.

## Exemples de questions

- « Je suis écrivain, en micro-BNC, 19 000 € de droits d'auteur sans précompte en 2026 : combien de cotisations, et est-ce que je dois le RAAP ? »
- « Mes revenus Patreon de 2025 n'ont jamais été déclarés : qu'est-ce que je risque, et comment je régularise proprement ? »
- « Je facture aussi des formations en micro-entreprise : comment s'articulent les deux régimes, et quelles franchises de TVA ? »

## Contenu

```
SKILL.md              instructions de l'agent
DISCLAIMER.md         avertissement (FR / EN)
data/                 valeurs chiffrées 2026, sourcées et datées (JSON)
references/           fiches : champ du régime, URSSAF, TVA, IR, plateformes, régularisation
examples/             cas travaillé : auteur sur plateforme + formateur en micro-entreprise
evals/                jeux de test (questions, sorties attendues, assertions)
scripts/              calculateur de cotisations et de RAAP
```

## Origine et crédits

Ce skill a été proposé au projet [paperasse](https://github.com/romainsimon/paperasse) de Romain Simon ([PR #76](https://github.com/romainsimon/paperasse/pull/76)), dont il reprend la structure et les conventions. Il est publié ici en dépôt autonome pour être utilisable sans attendre.

Il a été rédigé par un assistant IA sous la direction éditoriale de David Manise, à partir des sources officielles citées, et n'a pas été relu par un professionnel réglementé. Les corrections sourcées sont les bienvenues (issues et pull requests).

Licence MIT.
