# Régulariser des droits d'auteur non déclarés

*Textes consultés le 03/10/2026 : CGI art. 1727, 1728, 1729, 1758 A ; LPF art. L. 169 ; impots.gouv (« corriger ma déclaration », « délai de paiement »). Données machine : [`data/regularisation.json`](../data/regularisation.json). Volet social (URSSAF artistes-auteurs) : [urssaf-artistes-auteurs.md](urssaf-artistes-auteurs.md).*

## 1. Le cas typique

Un auteur encaisse depuis un ou deux ans des revenus de plateforme (Patreon, Substack, autoédition) en croyant que la plateforme « s'occupe des déclarations comme un éditeur ». Faux : une plateforme de paiement ne précompte rien et ne déclare rien à sa place (voir [plateformes.md](plateformes.md)). Rien n'a été déclaré ni au fisc ni à l'URSSAF.

**Posture du skill** : régularisation **spontanée**, avant tout contrôle, en choisissant le régime le moins coûteux parmi ceux qui sont légalement applicables. Pas de dissimulation.

## 2. Ce que coûte le passé — fisc (IR)

| Élément | Règle | Texte |
|---|---|---|
| Impôt sur les revenus omis | recalcul de l'IR de chaque année non prescrite avec les revenus ajoutés | — |
| Majoration — omission dans une déclaration déposée | 10 % de l'impôt éludé (20 % si dépôt tardif après mise en demeure), **écartée si correction spontanée** ou dans les 30 jours d'une demande | 1758 A |
| Majoration — déclaration catégorielle non déposée | 10 % sans mise en demeure ; 40 % au-delà de 30 j après mise en demeure ; 80 % activité occulte | 1728 |
| Manquement délibéré / manœuvres frauduleuses | 40 % / 80 % | 1729 |
| Intérêt de retard | **0,20 % par mois** depuis le 1er juillet N+1 ; **réduit de moitié** si dépôt spontané hors contrôle, bonne foi, paiement immédiat ou échéancier accepté | 1727 (V) |
| Prescription | fin de la 3e année suivant celle au titre de laquelle l'impôt est dû (revenus 2023 → 31/12/2026) ; 10 ans si activité occulte | LPF L. 169 |

Le choix 1758 A (omission dans une déclaration déposée) / 1728 (déclaration catégorielle non déposée) dépend de la situation : à faire valider.

## 3. Procédure (fisc)

1. **Année en cours de déclaration** (revenus 2025, en 2026) : service « Corriger ma déclaration » sur impots.gouv, du 29/07 au 30/11/2026. Hors période : messagerie sécurisée « Écrire > Réclamation/Contestation > Impôt sur le revenu », ou déclaration papier portant « DÉCLARATION RECTIFICATIVE, ANNULE ET REMPLACE ».
2. **Années antérieures non prescrites** : déclaration rectificative 2042 + 2042 C PRO pour chaque année.
3. **Pièces** : relevés de versements de la plateforme (export, API, relevés bancaires), total annuel par année.
4. **Courrier d'accompagnement** (facultatif mais utile) : exposer la bonne foi (erreur sur le rôle de la plateforme), demander l'application du 1727 V (intérêt réduit) et, si besoin, un délai de paiement.

## 4. Payer en plusieurs fois

- **Fisc** : délais de paiement « à titre exceptionnel » — messagerie sécurisée « Écrire > Paiement > Difficultés de paiement », formulaire 4805-S-SD + RIB + justificatifs (baisse de revenus, événement exceptionnel, endettement, antécédents de paiement). Réponse sous 2 mois (4 si complexe), silence = rejet ; recours au conciliateur fiscal départemental.
- **URSSAF artistes-auteurs** : échéancier sur demande (voir [urssaf-artistes-auteurs.md](urssaf-artistes-auteurs.md)).
- Un échéancier accepté par le comptable public ouvre droit à l'intérêt de retard réduit de 50 % (1727 V).

## 5. Ordre des opérations recommandé

1. Reconstituer les encaissements **par année civile** (plateforme + banque) → tableau.
2. Trancher le régime avec un expert-comptable : artiste-auteur (BNC ou TS si tiers déclarant) et, pour la TVA, le plafond applicable.
3. Affiliation / déclaration URSSAF artistes-auteurs pour les années concernées.
4. Déclarations rectificatives IR, année par année, avec courrier.
5. Demandes d'échéancier (URSSAF, fisc) si nécessaire.
6. Provisionner dès maintenant une fraction des encaissements courants (ordre de grandeur : 25 à 30 % selon le régime et la tranche d'imposition).

## 6. Ce qu'il ne faut pas faire

- Attendre « un contrôle » : les plateformes transmettent des données aux administrations (DAC7, selon la nature des opérations — voir [plateformes.md](plateformes.md)), et le passage à 40 % de majoration se joue sur la mise en demeure.
- Mélanger les années ou déclarer tout sur l'année en cours.
- Payer avec des fonds empruntés sans en avoir besoin : les échéanciers existent pour ça.
