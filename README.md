# Projet Tinder : qu'est-ce qui transforme une rencontre en match ?

Certification CDSD RNCP35288 - Bloc 2 : Analyse exploratoire, descriptive et inférentielle de données

## Contexte

L'équipe marketing de Tinder observe une baisse du nombre de matchs. Elle exploite une expérience menée entre 2002 et 2004 : des étudiants ont participé à des speed datings de 4 minutes, puis ont indiqué en secret s'ils voulaient revoir chaque partenaire. Un **match** a lieu quand les deux partenaires répondent « oui ».


## Objectif

Analyser le jeu de données pour tenter d'expliquer quels facteurs expliquent qu'une rencontre se transforme en match ?


## Données

Jeu de données 'dataset/dataset.csv'et son dictionnaire de variables, fournis par Jedha avec l'énoncé du projet.


## Etapes du projet

1. Imports et configuration
2. Découverte du jeu de données
3. Nettoyage et constitution des tables d'analyse
4. Profil des participants (analyse univariée)
5. Facteurs associés aux décisions (analyses descriptives et comparatives)
6. Quelques tests statistiques simples
7. Synthèse, recommandations et limites


## Principaux résultats

| # | Question | Résultat | 
|---|---|---|
| Q1 | Quelle proportion de rencontres aboutit à un match ? Existe-t-il une différence entre les sexes ? |16,5 % des rencontres aboutissent à un match. Les hommes disent plus souvent « oui » que les femmes (45,6 % contre 37,9 %).|
| Q2 | Quels critères distinguent les rencontres qui plaisent ? | L'attirance présente le plus grand écart de notes, suivie des intérêts communs ressentis et de l'humour. Les écarts de notes sont plus faibles pour la sincérité, l'intelligence et l'ambition. |
| Q3 | Les préférences déclarées correspondent-elles aux perceptions de l'autre sexe ? |Pas complètement : l'intelligence et la sincérité sont surdéclarées, tandis que l'humour et les intérêts communs sont sous-déclarés. Chaque sexe surestime de 8 à 9 points le poids de l'attirance chez l'autre.|
| Q4 | Les participants savent-ils évaluer leur propre valeur ? | Les participants s'attribuent en moyenne des notes supérieures à celles qu'ils reçoivent, avec des écarts allant de 0,75 à 1,27 point. Pour l'attirance, les groupes qui s'auto-évaluent le mieux reçoivent également de meilleures notes en moyenne.|
| Q5 | Les intérêts communs et l'origine commune favorisent-ils les matchs ? | L'origine commune est associée descriptivement à un taux de match légèrement supérieur (18,0 % contre 15,6 %). Les intérêts communs déclarés présentent une tendance positive pour les paires les plus proches, sans que sa significativité soit vérifiée. Les intérêts communs ressentis pendant la rencontre sont associés à des notes plus élevées lorsque le participant souhaite revoir son partenaire.|
| Q6 | Le moment de la rencontre influence-t-il la décision ? | Le premier rendez-vous présente un taux de décisions positives supérieur à celui des rencontres du milieu de soirée. Le taux du dernier rendez-vous est proche de celui du milieu.  |


## Limites

- Échantillon d'étudiants d'une même université (2002 - 2004), rencontre en face à face : la transposition à une application de swipe reste à prouver.
- Notes et décisions sont données au même moment (effet de halo) : les résultats décrivent des associations, pas des causes.
- Les rencontres d'un même participant ne sont pas indépendantes : les p-values peuvent être optimistes.
- 15,6 % des rencontres n'ont pas les six notes et ont un taux de « oui » plus faible (36,6 % contre 42,7 %).


## Structure du repo

```
cdsd_bloc2_projet_tinder/
├── assets
│   └── images
│       ├── 01_age_participants.png
│       ├── 02_domaine_d_etudes.png
│       ├── 03_objectif_participants.png
│       ├── 04_habitudes_participants.png
│       ├── 05_taux_decision_positive.png
│       ├── 06_notes_selon_decision.png
│       ├── 07_criteres_declares.png
│       ├── 08_criteres_vus_par_autre_sexe.png
│       ├── 09_auto_evaluation.png
│       ├── 10_ordre_rencontres.png
│       └── 11_origine_vs_interets.png
├── data
│   └── dataset.csv
├── notebook
│   └── projet_tinder.ipynb
├── README.md
└── requirements.txt          
```

## Installation

```pwershell
conda create -n cdsd_b2_projet_tinder python=3.11.17 pip -y
conda activate cdsd_b2_projet_tinder
python -m pip install -r requirements.txt    
```

# données brutes (8 378 rencontres, 195 colonnes)

