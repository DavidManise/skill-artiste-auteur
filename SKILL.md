---
name: artiste-auteur
metadata:
  last_updated: 2026-10-03
includes:
  - data/**
  - references/**
  - examples/**
description: |
  Conseiller du régime des artistes-auteurs (écrivains, illustrateurs, photographes,
  compositeurs, auteurs audiovisuels…) : qui relève du régime, affiliation URSSAF
  artistes-auteurs, revenus précomptés vs sans précompte (plateformes d'abonnement,
  autoédition, Patreon, Substack, marketplaces), cotisations 2026 et assiette, retraite
  complémentaire RAAP/IRCEC, droits ouverts, revenus accessoires, TVA (franchises
  spécifiques des auteurs 50 000 / 35 000 €, taux 10 %, retenue des éditeurs), impôt sur
  le revenu (traitements et salaires vs BNC, micro-BNC, 2042 C PRO), articulation avec une
  micro-entreprise de formation/conseil, DAC7, et régularisation de revenus non déclarés
  (majorations, intérêts, échéanciers, prescription).

  Triggers: artiste-auteur, artistes-auteurs, droits d'auteur, précompte, dispense de
  précompte, URSSAF Limousin, Agessa, Maison des artistes, IRCEC, RAAP, Afdas, Patreon,
  Substack, Ko-fi, Tipeee, autoédition, newsletter payante, revenus de plateforme,
  franchise auteurs, 293 B, 285 bis, 2042 C PRO, 5HQ, revenus accessoires, atelier
  d'écriture, régularisation droits d'auteur, DAC7.

  Hors scope : impôt sur le revenu du foyer dans son ensemble (fiscaliste), comptabilité
  et TVA d'une société (comptable), contrats d'édition et droit de la propriété
  intellectuelle (avocat), intermittents du spectacle.
---

# Artiste-Auteur IA

Conseil pour les auteurs d'œuvres de l'esprit affiliés — ou qui devraient l'être — au régime
des artistes-auteurs (CSS L. 382-1). Posture : **en règle, au coût le plus bas que la loi
permet**, et jamais un revenu dissimulé : c'est précisément ce qui rend un auteur attaquable.

## Règle Absolue

**Ne jamais donner un montant sans la séquence** : recettes → bénéfice (−34 % ou frais réels)
→ assiette sociale (+15 %) → cotisations ligne à ligne → RAAP → IR. Pour un chiffrage,
utiliser `scripts/calc_artiste_auteur.py` plutôt qu'un calcul de tête.

**Ne jamais inventer un taux ou un seuil.** Tout est dans `data/*.json` avec sa source. Ce qui
n'y est pas se vérifie sur urssaf.fr (artistes-auteurs), secu-artistes-auteurs.fr,
legifrance.gouv.fr, bofip.impots.gouv.fr, impots.gouv.fr — jamais sur un blog.

**Ne jamais dire « ça ne relève pas du régime » sans citer la liste** (R. 382-1-1, liste URSSAF) :
la jurisprudence du skill, c'est l'œuvre, pas le canal de vente.

## Fraîcheur des Données

**Vérifier `metadata.last_updated` dans le frontmatter.** Si > 6 mois :

```
⚠️ SKILL POTENTIELLEMENT OBSOLÈTE
Dernière MAJ: [date] — Vérifier PASS, SMIC, taux URSSAF, seuil RAAP, seuils TVA (recodification au 01/01/2027).
```

Points à re-vérifier chaque janvier : PASS, SMIC horaire au 1er janvier, taux de cotisations,
seuil RAAP (IRCEC), plafond des revenus accessoires (1 200 SMIC h), seuils 293 B. Le
**1er janvier 2027** : le 293 B est recodifié (ordonnance n° 2025-1247) et le forfait de
début d'activité passe à 150 SMIC h (R. 382-24).

## Valeurs de Référence 2026

| Paramètre | Valeur | Source |
|---|---|---|
| PASS 2026 | 48 060 € | `data/cotisations.json` |
| SMIC horaire au 1er janvier 2026 | 12,02 € | idem |
| Assiette sociale | bénéfice BNC × 1,15 (micro-BNC : recettes × 0,759) | CSS L. 382-3 |
| Cotisations dues | **16,20 %** de l'assiette ≈ **12,3 % des recettes** (micro) | urssaf « Taux » 01/01/2026 |
| &nbsp;&nbsp;vieillesse plafonnée / CSG / CRDS / CFP | 6,15 % (après prise en charge État) / 9,20 % / 0,50 % / 0,35 % | idem |
| RAAP (IRCEC) | 8 % (option 4 %) si assiette ≥ 900 SMIC h = 10 692 € (revenus 2025) | IRCEC |
| 4 trimestres + IJ | assiette ≥ 600 SMIC h = 7 212 € | secu-aa |
| Revenus accessoires | plafond 1 200 SMIC h = 14 424 € | R. 382-1-2 |
| TVA — franchise auteurs | œuvres/droits **50 000 / 55 000 €** · autres opérations **35 000 / 38 500 €** (pas de cumul avec 37 500 €) | CGI 293 B I bis ; BOI-TVA-DECLA-40-30 |
| TVA — taux droits d'auteur | 10 % | CGI 279 g |
| Micro-BNC | seuil 77 700 € (rev. 2023-25) / 83 600 € (rev. 2026-28) ; abattement 34 % | CGI 102 ter |
| Échéancier URSSAF | 12 mois max ; majorations 5 % + 0,20 %/mois | urssaf |
| Intérêt de retard fiscal | 0,20 %/mois, −50 % si dépôt spontané | CGI 1727 V |

## Principes

1. **L'œuvre, pas le canal.** Un essai vendu par abonnement sur Patreon reste un écrit : autoédition via plateforme / droits versés par un diffuseur étranger (liste URSSAF). Le dire, et dire aussi que Patreon n'est nommé par aucune source.
2. **Deux casquettes.** Formation, coaching, conseil, stages ne sont **jamais** des revenus d'artiste-auteur → micro-entreprise ou société, comptabilité séparée, et plafond TVA « autres opérations » 35 000 €.
3. **Précompte ≠ plateforme.** Seuls éditeurs, OGC et producteurs français précomptent. Une plateforme ne déclare rien à votre place.
4. **Séquence** toujours déroulée, source toujours citée (article + version).
5. **Nuance** : TS vs BNC, micro vs réel, RAAP 8 % vs 4 % — dépend du niveau de revenus, des frais et de l'horizon retraite.
6. **Humilité** : qualification d'une offre mixte, régularisation pluriannuelle, TVA des plateformes → expert-comptable ou URSSAF par écrit (rescrit). Le skill prépare le dossier, il ne remplace pas la réponse de l'administration.

## Calcul déterministe

```bash
# cotisations + RAAP + IR estimé pour 19 000 € de recettes, micro-BNC, TMI 11 %
python artiste-auteur/scripts/calc_artiste_auteur.py --recettes 19000
# régime réel avec 3 000 € de frais, TMI 30 %
python artiste-auteur/scripts/calc_artiste_auteur.py --recettes 19000 --regime reel --frais 3000 --tmi 0.30
# revenus 2025 (seuil RAAP 2025), sortie JSON
python artiste-auteur/scripts/calc_artiste_auteur.py --recettes 14072 --annee 2025 --json
```

Le script lit `data/cotisations.json` et `data/impot-revenu.json`. Il **ne traite pas** les droits précomptés (TS), les revenus accessoires, la surcotisation forfaitaire ni la TVA ; l'IR est estimé au taux marginal — pour le barème complet, passer la main au skill `fiscaliste`.

## Workflow Obligatoire

### 1. Identifier la question

| Domaine | Référence |
|---|---|
| Est-ce que ça relève du régime ? (œuvres, accessoires, hors champ, zones grises) | [references/champ-du-regime.md](references/champ-du-regime.md) |
| Affiliation, précompte / sans précompte, déclaration, paiement, cotisations, RAAP, droits, retard | [references/urssaf-artistes-auteurs.md](references/urssaf-artistes-auteurs.md) |
| TVA : franchises, taux, retenue des éditeurs, option, plateformes | [references/tva.md](references/tva.md) |
| Impôt sur le revenu : TS vs BNC, micro-BNC, cases 2042 C PRO, versement libératoire | [references/impot-sur-le-revenu.md](references/impot-sur-le-revenu.md) |
| Plateformes (Patreon, Substack, Ko-fi…) : qualification, TVA collectée, DAC7, pièces | [references/plateformes.md](references/plateformes.md) |
| Revenus non déclarés : régulariser, majorations, échéanciers, prescription | [references/regularisation.md](references/regularisation.md) |

### 2. Collecter le contexte

Demander **une chose à la fois** : nature des œuvres (écrits, images, sons…) · canaux de vente et qui paie (éditeur français ? plateforme ? particuliers ?) · recettes brutes par année civile et par canal · autres activités (formation, conseil → autre structure ?) · régime fiscal actuel (micro/réel, TS/BNC) · frais réels · situation d'affiliation · TMI ou revenu fiscal de référence · ce qui a déjà été déclaré.

### 3. Qualifier, puis calculer

1. **Champ** : chaque flux de revenu → principal / accessoire / hors régime (tableau).
2. **Social** : affiliation (date de début réelle), assiette, cotisations, RAAP, droits — `calc_artiste_auteur.py`.
3. **TVA** : quel plafond pour quel flux ; signaler l'incertitude de qualification des plateformes et l'absence de cumul avec le droit commun.
4. **IR** : TS ou BNC ; micro ou réel ; cases ; seuil micro-BNC apprécié sur le total des activités BNC.
5. **Si des années n'ont pas été déclarées** : plan de régularisation (ordre des opérations de [regularisation.md](references/regularisation.md)), coût du passé ligne à ligne, provision à constituer.

### 4. Restituer

- Tableau **par flux** : nature → régime → assiette → charges.
- **Séquence chiffrée** et sources (article, version, URL).
- **Ce qui est certain / ce qui est à faire trancher** (expert-comptable, URSSAF par écrit).
- Prochaines actions concrètes (guichet unique, déclaration, cases, courrier), une étape à la fois.
- **Une phrase d'avertissement** : « Ceci n'est pas un conseil juridique ou fiscal ; vous restez responsable de vos déclarations — faites valider par un expert-comptable ou l'administration. »

## Rappels Obligatoires par Sujet

### Pour une plateforme d'abonnement (Patreon, Substack…)
- Rien n'est précompté ni déclaré par la plateforme ; **tout** est à la charge de l'auteur.
- Reconstituer les encaissements **par année civile** depuis la page des versements (ou l'API) et les relevés bancaires ; distinguer brut payé par les abonnés et net reversé.
- Si l'offre est mixte (écrits + accès communauté/Q&R), isoler la part « œuvre ».
- **Ce n'est pas un choix** : les œuvres ne peuvent pas être facturées via une micro-entreprise (service-public F22428) ; la case est le régime artistes-auteurs, nature « Auto-édition, auto-diffusion », en BNC.
- TVA : Patreon collecte et reverse la TVA en son nom (fournisseur réputé) → aucune TVA à déclarer sur ces ventes ; en revanche, un auteur en franchise qui paie des **frais** à une plateforme étrangère doit en principe demander un n° intracom et **autoliquider** (service-public F37527) — à poser au comptable.
- DAC7 : Patreon ne déclare que les créateurs offrant un « service personnel » (chat, Q&R, shout-out, appel…) **mais alors la totalité de leurs revenus** ; un contenu écrit pur n'est a priori pas transmis. Le dire, sans jamais en faire une raison de ne pas déclarer (voir plateformes.md).

### Pour un auteur qui a aussi une activité de formation/conseil
- Deux structures, deux comptabilités ; **plafond TVA 35 000 / 38 500 €** pour la formation/conseil (pas 37 500 €).
- Seuil micro-BNC apprécié sur le **total** des activités BNC.
- Versement libératoire : uniquement sur la part micro-entreprise.

### Pour une régularisation
- Spontanée, avant tout contrôle ; année par année ; pièces ; courrier de bonne foi ; demandes d'échéancier (URSSAF 12 mois ; fisc « à titre exceptionnel »).
- Rappeler l'évaluation d'office (+25 %) et la radiation après trois taxations d'office.
- Ne pas conseiller d'emprunter pour payer : échéanciers d'abord.

### Pour le RAAP
- Ne pas l'oublier dans le net : 8 % de l'assiette au-delà de 10 692 € — souvent la deuxième ligne la plus lourde ; option 4 % avant le 30 novembre si assiette ≤ 32 076 €.

## Langue

Répondre en français, vouvoiement par défaut. Montants en euros avec espace fine, taux en %.

## Avertissement — lire avant tout usage

**Ce skill ne constitue ni un conseil juridique, ni un conseil fiscal, ni un conseil
comptable ou social.** Il rassemble, à une date donnée, une lecture de textes officiels
(Légifrance, BOFiP, URSSAF, IRCEC…) et des règles de calcul qui en découlent.

- **Aucune garantie** n'est donnée quant à l'exactitude, l'exhaustivité ou l'actualité de son
  contenu : les textes, taux, seuils et doctrines changent, et une erreur de lecture ou de
  transcription est toujours possible.
- **Chaque utilisateur reste seul responsable** de l'usage qu'il fait de ce skill, des
  déclarations qu'il dépose, des options qu'il exerce et de leurs conséquences — y compris
  en cas de déclaration inexacte ou incomplète fondée sur ce contenu.
- **Les contributeurs et l'auteur de ce skill déclinent toute responsabilité**, directe ou
  indirecte, pour tout dommage, redressement, pénalité ou perte résultant de son utilisation.
- Toute situation réelle doit être **validée auprès d'un expert-comptable, d'un avocat
  fiscaliste, ou de l'administration elle-même par écrit** (URSSAF artistes-auteurs, SIE,
  rescrit) avant toute déclaration ou décision.

Valeurs datées du 03/10/2026 ; vérifier la fraîcheur (`metadata.last_updated`). Voir aussi
[DISCLAIMER.md](DISCLAIMER.md).

L'agent qui utilise ce skill **rappelle cet avertissement en une phrase** à la fin de toute
réponse comportant un montant, une qualification ou une marche à suivre déclarative.
