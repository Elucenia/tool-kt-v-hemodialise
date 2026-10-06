<!-- ELUCENIA technical documentation · kt-v-hemodialise · fr · no clinical/professional/rights approval -->

# Kt/V et URR en hémodialyse

[conditions, sources et autorisations](https://elucenia.org/fr/outils/kt-v-hemodialise)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Urée avant dialyse

`pre`

mg/dL · intervalle: 10–500

### Urée après dialyse

`pos`

mg/dL · intervalle: 2–400

### Durée de la séance

`horas`

heures · intervalle: 1–10

### Ultrafiltration (perte de poids)

`uf`

L (kg) · intervalle: 0–8

### Poids après dialyse

`peso`

kg · intervalle: 20–250

## Édition de la méthode

Daugirdas 2e génération 1993 : spKt/V variable ; UF/poids après ; URR ; sans Kt/V équilibré

## Formule documentée

spKt/V = −ln(R − 0,008 × t) + (4 − 3,5 × R) × UF ÷ P

R = urée après ÷ urée avant; t = durée (h); UF = ultrafiltration (L); P = poids après dialyse (kg).

URR (%) = (1 − R) × 100.

## Limites et population

Cette formule estime le spKt/V d’une séance, avec un compartiment unique et une correction de volume, et n’équivaut pas au Kt/V équilibré ou hebdomadaire. La technique, le moment des prélèvements, les unités et le schéma de dialyse doivent correspondre à la méthode. Les objectifs KDOQI ont leur propre contexte et source ; l’analyse de la valeur seule ne confirme pas l’adéquation globale du traitement.

## Références

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

spKt/V ≥ 1,4 : atteint la cible KDOQI 2015

| Détails du résultat | |
| --- | --- |
| Taux de réduction de l'urée (URR) | 70,0 % |
| Rapport post/pré (R) | 0,300 |


### 2

spKt/V entre 1,2 et 1,4 : au-dessus du minimum, en dessous de la cible

| Détails du résultat | |
| --- | --- |
| Taux de réduction de l'urée (URR) | 65,0 % |
| Rapport post/pré (R) | 0,350 |


### 3

spKt/V < 1,2 : dialyse inadéquate

| Détails du résultat | |
| --- | --- |
| Taux de réduction de l'urée (URR) | 60,0 % |
| Rapport post/pré (R) | 0,400 |

URR inférieur à 65%.

