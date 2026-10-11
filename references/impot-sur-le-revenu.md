# Impôt sur le revenu des droits d'auteur — régimes, seuils, cases

*Revenus 2025 (déclaration 2026) et revenus 2026. Textes consultés le 03/10/2026 : CGI art. 93 1 quater, 102 ter (version 01/07/2026), 151-0, 241 ; BOI-BNC-SECT-20-10-20 ; BOI-BNC-DECLA-20-10-20260819 ; formulaire 2042 C PRO 2026 (n° 11222*28). Données machine : [`data/impot-revenu.json`](../data/impot-revenu.json).*

## 1. Deux portes d'entrée selon QUI verse les droits

| Situation | Régime IR par défaut | Cases |
|---|---|---|
| Droits **intégralement déclarés par des tiers** tenus à la déclaration de l'art. 241 (éditeurs, SACEM, SACD, producteurs…) | **Traitements et salaires** (CGI 93, 1 quater) : abattement 10 % sur (brut − cotisations sociales obligatoires), ou frais réels | 2042 : **1GF / 1HF / 1IF / 1JF** (frais réels : 1AK à 1DK) |
| Droits **non déclarés par des tiers** : plateformes d'abonnement, autoédition, ventes directes | **BNC** (micro-BNC ou déclaration contrôlée) | 2042 C PRO (voir §3) |

Texte (93, 1 quater) : « Lorsqu'ils sont intégralement déclarés par les tiers, les produits de droits d'auteur perçus par les auteurs des œuvres de l'esprit mentionnées à l'article L. 112-2 du code de la propriété intellectuelle sont […] soumis à l'impôt sur le revenu selon les règles prévues en matière de traitements et salaires. »

L'auteur en TS peut **opter pour les BNC** (via la 2042 C PRO) ; l'option vaut pour l'année et les deux suivantes. Inversement, sans tiers déclarant, le régime TS est refusé (BOI-BNC-SECT-20-10-20 §50) : **les abonnements Patreon/Substack relèvent a priori des BNC**. Point ouvert : une plateforme étrangère qui transmet des données DAC7 est-elle un « tiers déclarant » au sens de l'art. 241 ? Aucune position administrative connue.

## 2. Micro-BNC (CGI 102 ter)

| Paramètre | Valeur |
|---|---|
| Seuil de recettes HT (N-1 ou N-2) — revenus 2023 à 2025 | **77 700 €** |
| Seuil — revenus 2026 à 2028 (décret n° 2026-562 du 29/06/2026) | **83 600 €** |
| Abattement forfaitaire pour frais | **34 %** (minimum 305 €) |
| Maintien du micro après dépassement | les deux premières années de dépassement |

**Pluralité d'activités BNC** (102 ter, 6 a ; BOI-BNC-DECLA-20-10 §170-180) : « les recettes des différentes activités doivent être totalisées pour apprécier le seuil » ; en cas de dépassement, exclusion du micro **pour l'ensemble** des activités. Les droits imposés en TS ne comptent pas, sauf option BNC. → Un auteur en BNC qui a aussi une micro-entreprise de conseil additionne les deux pour le seuil (77 700 € / 83 600 €) — ce qui laisse en général beaucoup de marge, contrairement aux plafonds de TVA (voir [tva.md](tva.md)).

Exclusion : auteurs pour lesquels la retenue de TVA de l'art. 285 bis est appliquée (fiche DGFiP 2026).

**Déclaration contrôlée** : formulaire 2035 ; option au titre de 2026 possible jusqu'au 20/05/2027, reconduction tacite. Utile si les frais réels dépassent 34 % des recettes.

## 3. Cases de la 2042 C PRO 2026 (revenus 2025)

| Situation | Déclarant 1 / 2 / personne à charge |
|---|---|
| Micro-BNC **professionnel** — recettes brutes encaissées, abattement 34 % appliqué par l'administration | **5HQ / 5IQ / 5JQ** |
| Déclaration contrôlée (bénéfice 2035) | 5QC / 5RC / 5SC |
| Micro-entrepreneur ayant opté pour le versement libératoire (BNC) | 5TE / 5UE / 5VE |
| BNC **non professionnels**, micro | 5KU / 5LU / 5MU |
| Droits d'auteur en traitements et salaires (2042) | 1GF / 1HF / 1IF / 1JF |

Les droits d'auteur d'une activité exercée à titre habituel et lucratif sont des BNC **professionnels** (5HQ…), pas « non professionnels » (5KU), réservés aux activités occasionnelles.

## 4. Versement libératoire de l'IR (CGI 151-0)

Taux **2,2 %** des recettes BNC, payé avec les cotisations. Trois conditions **cumulatives** :
1. relever du micro (50-0 ou 102 ter) ;
2. RFR du foyer de N-2 ≤ limite supérieure de la 2e tranche du barème **par part** (pour 2026 : RFR 2024 ≤ 29 315 €/part, +50 % par demi-part, +25 % par quart de part) ;
3. être soumis au **régime micro-social** de l'art. L. 613-7 CSS (micro-entrepreneur).

Un artiste-auteur est affilié au régime général au titre de l'art. L. 382-1 CSS, pas au micro-social : **le versement libératoire ne peut couvrir que les recettes de la micro-entreprise, pas les droits d'auteur** (lecture des textes, à confirmer par l'expert-comptable). Option auprès de l'URSSAF avant le 30 septembre de N pour N+1.

## 5. Séquence de calcul (micro-BNC, droits d'auteur sans tiers déclarant)

1. Recettes brutes encaissées dans l'année (relevés de la plateforme, versements bancaires).
2. Bénéfice imposable = recettes × (1 − 0,34).
3. Ajout aux autres revenus du foyer → barème progressif (voir skill `fiscaliste` : quotient familial, décote).
4. Pas de prélèvements sociaux « revenus du patrimoine » : les cotisations sociales sont celles du régime artistes-auteurs (voir [urssaf-artistes-auteurs.md](urssaf-artistes-auteurs.md)) — CSG/CRDS incluses, dont une fraction de CSG déductible l'année suivante.
5. Exemple : 19 000 € de recettes → 12 540 € imposables → à 11 % de TMI ≈ 1 380 € ; à 30 % ≈ 3 760 €. Toujours montrer la séquence.
