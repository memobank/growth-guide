---
layout: default
title: Churn
description: Découvrez comment calculer votre taux d’attrition (churn).
image: /assets/images/cards/card-indicateurs-churn.png
parent: Indicateurs
---

# Le churn (ou taux d’attrition)

Le _churn_, ou taux d’attrition en français, représente le pourcentage de clients que vous perdez sur une période donnée — un mois, un trimestre, une année.

Le _churn_ est surtout suivi par les entreprises SaaS. Ces entreprises ont un modèle d’affaires par abonnement, qui rend le suivi de leur activité prévisible. Chaque client génère un revenu récurrent, qui se répète chaque mois, ou chaque année — jusqu’à ce qu’il résilie son abonnement. Combiné au calcul des revenus récurrents, le _churn_ permet aux entreprises SaaS d’estimer leurs revenus à venir — et d’ajuster leur modèle en conséquence.

## Deux types de churn

Les entreprises innovantes calculent souvent deux types de churn :

1. Le _churn_ client (_logo churn_, ou _customer churn_ en anglais), qui mesure la perte du nombre de clients sur une période donnée ;
2. Le _churn_ de revenu (_revenue churn_ en anglais), qui mesure la perte de revenu récurrent causée par la perte de clients sur une période donnée.

Le calcul du _churn_ de revenu est particulièrement important lorsque vous commercialisez différentes formules d’abonnement, des options payantes, ou des produits différents. Le départ de vos clients peut avoir des conséquences très différentes sur votre revenu récurrent, en fonction du type de clients que vous perdez — des clients abonnés à votre formule la plus économique, ou des clients abonnés à votre formule la plus chère. Or, le _churn_ client ne vous donne qu’un chiffre global des clients perdus, il ne vous renseigne pas sur le poids de tel ou tel client dans vos revenus totaux.

## Le churn client

### Définition et formule

Le _churn_ client mesure la perte de vos clients sur une période donnée. Ce _churn_ est un pourcentage, résultat du rapport entre le nombre de clients que vous perdez sur la période choisie (un mois, un trimestre, une année), et le nombre de clients que vous aviez au début de cette période.

La formule du _churn_ client sur une période donnée est :

```
Churn client = Nombre de clients perdus sur la période / Nombre de clients au début de la période
```

#### Exemple de calcul

Vous souhaitez calculer votre _churn_ client du mois d’avril. Le 31 mars, vous aviez 120 clients. Vous faites le bilan le 30 avril : vous avez perdu 4 clients.

Votre _churn_ mensuel est donc :

```
Churn client (avril) = 4 / 120 * 100 = 3 %
```

### Période de calcul idéale

Vous pouvez en théorie calculer un _churn_ pour n’importe quelle période. Cependant, toutes les périodicités ne seront pas pertinentes pour votre entreprise : vous devez choisir celle qui est cohérente avec vos formules d’abonnement.

Si vos clients vous paient _à l’année_, par exemple, évitez de calculer un _churn mensuel_. Vos clients ne prennent la décision de prolonger ou non leur contrat qu’une fois par an. Un mois donné, la plupart de vos clients ne sont pas dans la possibilité de vous quitter : vous risquez d’obtenir un _churn_ sous-évalué, qui ne reflète pas l’engagement de vos clients.

### Excluez de votre churn les clients qui ne peuvent pas résilier

Si vous incluez dans le calcul de votre _churn_ sur une période donnée, des clients qui ne peuvent pas résilier leur abonnement sur cette période, vous risquez de sous-évaluer votre _churn_. Plusieurs situations peuvent expliquer que sur une période donnée, tous vos clients ne puissent pas résilier leur abonnement :

- Premier exemple : vous calculez votre _churn_ sur une base mensuelle, mais certains de vos clients vous paient au mois, d’autres à l’année. Il est probable que lors d’un mois donné, un certain nombre de vos clients qui vous paient sur une base annuelle ne soient pas en mesure de résilier leur contrat.
- Second exemple : vous imposez à vos nouveaux clients une période minimale d’engagement, par exemple de trois mois.

Dans ce type de situations, vous devriez exclure du calcul de votre _churn_ les clients qui ne peuvent pas résilier leur abonnement, au risque de sous-évaluer votre churn. Calculez votre _churn_ sur la base des clients qui peuvent réellement interrompre leurs abonnements.

La nouvelle formule de votre _churn_ client dans ce cas devient :

Churn client = Nombre de clients perdus au cours de la période T / (Nombre total de clients existants au début de la période T - Nombre de clients ne pouvant pas résilier sur la période T)

#### Exemple de calcul

Vous souhaitez calculer votre _churn_ mensuel au mois d’avril. Vous avez au 31 mars 120 clients, qui paient des abonnements mensuels. Durant le mois d’avril, vous perdez 9 clients.

Votre _churn_ mensuel est donc :

```
Churn (avril) = 9 / 120 * 100 = 7,5 %
```

Lorsque vos clients vous rejoignent, ils s’engagent à payer leurs abonnements pour trois mois minimum. Sur votre base de clients, un certain nombre de clients ne pouvaient donc pas résilier leurs abonnements en avril : les clients qui vous ont rejoint en février et en mars sont au nombre de 15.

Votre _churn_ mensuel ajusté devient donc :

```
Churn (avril) = 9 / (120 - 15) * 100 = 8,6 %
```

### Limites du churn mensuel

S’il n’est pas utile pour toutes les entreprises SaaS de calculer un _churn_ mensuel, toutes devraient calculer leur _churn_ annuel. Votre _churn_ mensuel peut sembler normal, mais devient très important lorsqu’il est calculé sur une base annuelle.

#### Exemple de calcul

Reprenons notre exemple précédent. Vous avez donc perdu 9 clients au mois d’avril, et en aviez 120 à la fin du mois précédent. Votre _churn_ est de 7,5 %.

Ce _churn_ semble tout à fait acceptable. Pourtant, il devient beaucoup plus inquiétant lorsqu’il est rapporté à l’année. Imaginons que vous continuiez à perdre 9 clients tous les mois, pendant les douze prochains mois. Votre _churn_ annuel sera donc :

```
Churn annuel = (9 * 12) / 120 * 100 = 90 %
```

Cela signifie que vous avez perdu 90 % de vos clients en un an. Pour garder le même niveau de revenu, vous devriez donc attirer presque autant de nouveaux clients que ce que vous en avez aujourd’hui.

### Interprétations du _churn_ client

Que déduire du pourcentage de votre churn ? Votre situation est-elle inquiétante, normale ou avantageuse, par rapport à la moyenne des entreprises SaaS ?

Il est difficile de dire ce qu’est un « bon » _churn_ pour votre entreprise. Il faudrait pouvoir comparer votre entreprise à d’autres entreprises du même secteur, avec la même ancienneté, avec un niveau de [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) comparable, dans la même région… Malheureusement, trop peu d’entreprises publient leur churn.

Des études permettent toutefois de disposer de fourchettes de _churn_ qui vous aideront à vous faire une idée. L’agence Cobloom a publié en juillet 2020 un [article](https://www.cobloom.com/blog/churn-rate-how-high-is-too-high#) qui synthétise des études menées aux États-Unis auprès de quelques centaines d’entreprises SaaS.

Deux catégories d’entreprises semblent émerger :

- **Les entreprises dont le MRR est supérieur à 1 million de dollars affichent en moyenne des churns entre 5 et 15 %.**
- **Les entreprises dont le MRR est inférieur à 1 millions de dollars affichent des fourchettes de _churn_ beaucoup plus larges, de 5 à 90 %.**

Deux facteurs peuvent expliquer ces écarts de _churn_ en fonction de la taille de l’entreprise :

- L’ancienneté de l’entreprise : les entreprises dont le [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) est inférieur à 1 million de $ sont pour la plupart des entreprises jeunes, qui construisent leurs produits en même temps qu’elles découvrent les besoins réels de leurs clients. Il est courant que dans les premières années d’existence d’une start-up, le _churn_ soit plus élevé : soit parce que la start-up ne s’est pas adressée aux bons clients, soit qu’elle n’a pas encore développé le produit dont sa cible a besoin. A contrario, les entreprises au [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) supérieur sont soit des entreprises qui ont rapidement rencontré du succès, soit des entreprises qui ont plusieurs années d’existence. Elles ont réussi à développer un produit qui a rencontré son marché — les entreprises qui ne réussissent pas font faillite après quelques années. Celles qui survivent, et ont un [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) important, ont mécaniquement un _churn_ tendanciellement moins important.
- La typologie de clients auxquels s’adressent ces entreprises : les clients des entreprises SaaS les plus importantes sont souvent des grandes entreprises. Les cycles de ventes auprès des grands groupes sont plus longs, mais ces clients s’engagent généralement à plus long terme — et ils sont plus fidèles. De plus, ces entreprises sont en général abonnées au mois. Les entreprises dont le [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) est moins important s’adressent plutôt à des particuliers ou des PME, dont les comportements sont plus volatils — et qui sont plus sensibles au prix, et au basculement vers la concurrence dès que celle-ci propose des prix plus compétitifs.

## Le churn de revenu

### Définition et formule

Le _churn_ de revenu mesure le montant de revenu récurrent que vous perdez sur une période donnée, à cause de la perte de vos clients sur cette période. Le _churn_ de revenu se calcule à partir des indicateurs mesurant le revenu récurrent d’une entreprise sur une période, comme le [MRR]({% link indicateurs/monthly-recurring-revenue.md %}), l’ARR, le Churn MRR et le Churn ARR.

- Le [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) est votre « revenu mensuel récurrent », et l’ARR votre « revenu annuel récurrent » : c’est-à-dire la somme des revenus récurrents sur un mois ou une année donnés. En général, pour une entreprise SaaS, ces revenus récurrents sont la somme des abonnements en ligne, et des éventuelles options récurrentes payées par les clients.
- Le Churn MRR, ou le Churn ARR, mesurent les pertes de revenu récurrent causées par le départ de vos clients, sur un mois ou une année.

Le _churn_ du revenu d’une période donnée est le rapport entre le _churn_ MRR/ARR de cette période, et le MRR/ARR de votre entreprise au début de cette période.

```
Churn de revenu (mois) = Churn MRR / MRR * 100
Churn de revenu (année) = Churn ARR / ARR * 100
```

#### Exemple de calcul

Vous souhaitez calculer votre _churn_ de revenu au mois d’avril. Vous aviez au 31 mars 120 clients, qui paient des abonnements mensuels. 60 de vos clients sont abonnés à votre formule Simple à 50 € par mois, et 60 de vos clients sont abonnés à votre formule Premium à 100 € par mois.

Durant le mois d’avril, vous perdez 9 clients : 6 clients sur votre formule Simple, et 3 clients sur votre formule Premium.

Votre Churn MRR en avril et votre MRR en mars sont :

```
Churn MRR (avril) = 6 * 50 € + 3 * 100 € = 600 €
MRR (mars) = 60 * 50 € + 60 * 100 € = 9 000 €
```

Votre _churn_ de revenu sur le mois d’avril est donc :

```
Churn de revenu (avril) = Churn MRR (avril) / MRR (mars) * 100
			= 600 / 9 000 * 100
			= 6,7 %
```

Nous n’incluons dans le _churn_ du revenu, que les pertes de revenu récurrent causées par le _départ_ de vos clients — le rapport entre le Churn MRR et le [MRR]({% link indicateurs/monthly-recurring-revenue.md %}). Certaines entreprises incluent également dans le _churn_ du revenu les pertes de revenu récurrent qui sont la conséquence du _downgrade_ de vos client, c’est-à-dire de leur passage à de formules d’abonnement inférieures, ou sans option payante — le rapport entre le Contraction MRR (cf. l’article sur le [MRR]({% link indicateurs/monthly-recurring-revenue.md %})) et le MRR.

Vous pouvez utiliser le Contraction MRR pour calculer le pourcentage de revenu récurrent qui diminue en raison du passage de vos clients à des formules d’abonnement inférieures, ou de la résiliation d’options payantes :

```
Contraction du revenu (mois) = Contraction MRR / MRR * 100
```

Vous pouvez utiliser le Churn MRR et le Contraction MRR pour évaluer un _churn_ « global », qui inclut à la fois la perte de revenus issue de la résiliation de vos clients, et la perte de revenus issue des _downgrades_ de vos clients existants — qui restent vos clients.

```
Churn de revenu global (mois) = (Churn MRR + Contraction MRR) / MRR * 100
```

### Le churn du revenu net

Même si votre _churn_ de revenu sur un mois donné est supérieur à 0, il est possible que vos clients existants vous aient fait gagner plus d’argent sur ce mois que le mois précédent. C’est par exemple le cas lorsque les plus-values de revenu récurrent issues du passage de vos clients à des formules d’abonnement supérieures, soit supérieur aux moins-values de revenu récurrent issues du désengagement de vos clients.

Le _Net revenue churn_, ou _churn_ du revenu net, s’intéresse donc au revenu récurrent que vos clients _existants_ vous ont fait perdre, ou gagner, sur une période donnée. Cet indicateur ne prend donc pas en compte les revenus issus de vos _nouveaux_ clients sur une période donnée.

Il se calcule ainsi (sur une période mensuelle) :

```
Churn du revenu net = (Churn MRR + Contraction MRR + Expansion MRR) / MRR du mois précédent
```

« L’Expansion MRR » est un indicateur qui mesure, sur un mois donné, l’augmentation de revenu récurrent de la part de vos clients existants : passage à des formules d’abonnement supérieures, souscriptions d’option payantes, etc.

Le _churn_ du revenu net peut être négatif : dans ce cas, il signifie que vous avez généré davantage de revenu récurrent sur vos clients existants, sur un mois donné, par rapport au mois précédent.

#### Exemple de calcul

Vous souhaitez calculer votre _churn_ de revenu net au mois d’avril. Vous aviez au 31 mars 120 clients, qui paient des abonnements mensuels. 60 de vos clients sont abonnés à votre formule Simple à 50 € par mois, et 60 de vos clients sont abonnés à votre formule Premium à 100 € par mois.

Au mois d’avril :

- vous perdez 9 clients : 6 clients sur votre formule Simple, et 3 clients sur votre formule Premium ;
- 5 de vos clients abonnés à votre formule Premium s’abonnent à votre formule Simple ;
- 20 de vos clients abonnés à votre formule Simple s’abonnent à votre formule Premium.

Nous avons donc :

```
MRR (mars) = (60 * 50 € + 60 * 100 €) * 100 = 9 000 €
Churn MRR (avril) = 6 * 50 € + 3 * 100 € = 600 €
Contraction MRR (avril) = 5 * (100 € - 50 €) = 250 €
Expansion MRR (avril) = 20 * (100 € - 50 €) = 1 000 €
```

Votre churn de revenu net est donc :

```
Churn de revenu net (avril) = (600 + 250 - 1 000) / 9 000 = -1,7 %
```

### Interprétation du churn de revenus

#### Le MRR

D’après une étude de l’entreprise [Profitwell](https://www.profitwell.com/recur/all/average-revenue-churn-rate-benchmarks#:~:text=If%20your%20average%20revenue%20per,closer%20to%203%2D4%25.), le _churn_ de revenu n’est corrélé avec le MRR que pour les entreprises dont le MRR est élevé :

- les entreprises dont le MRR est inférieur à 500 000 $ ont un _churn_ entre 3 % et 16 % ;
- les entreprises dont le MRR est entre 500 000 $ et 1 million $ ont un _churn_ entre 3 % et 8,5 % ;
- les entreprises dont le MRR est supérieur à 1 million $ ont un _churn_ entre 2 et 8 %.

#### L’âge de l’entreprise

D’après cette même étude, le _churn_ de revenu est fortement corrélé avec l’âge de l’entreprise. Plus l’entreprise est ancienne (c’est-à-dire plus elle a survécu longtemps), plus son _churn_ de revenu est faible. Une entreprise plus ancienne qui a survécu a établi son business model, trouvé ses clients, et le bon produit pour ses clients — sinon elle aurait fait faillite. Elle a construit un produit qui satisfait ses clients :

- les entreprises de moins d’un an ont un _churn_ entre 7 % et près de 25 % ;
- les entreprises entre 1 et 3 ans ont un _churn_ entre 4 % et près de 15 % ;
- les entreprises entre 3 et 10 ans ont un _churn_ entre 2 % et 9 % ;
- les entreprises de plus de 10 ans ont un _churn_ entre 2 et 4 %.

#### Le revenu moyen par utilisateur

Le _churn_ de revenu est également corrélé avec le revenu moyen par utilisateur. Plus les utilisateurs dépensent, plus ils tendent à rester fidèle à l’entreprise dont ils sont clients :

- les entreprises dont le revenu moyen par utilisateur est inférieur à 50 $ ont un _churn_ compris entre 5 et 16 %, et un _churn_ médian entre 8 et 9,5 % ;
- les entreprises dont le revenu moyen par utilisateur est entre 50 et 500 dollars ont un _churn_ compris entre 3 % et 14 %, et un _churn_ médian entre 6 et 7 % ;
- les entreprises dont le revenu moyen est supérieur à 500 $ ont un _churn_ compris entre 2 % et 7 %, et un _churn_ médian entre 2,5 % et 5 %.

Autre source comparative disponible en ligne : [l’édition 2021](https://www.key.com/kco/images/2021_kbcm_saas_survey_final.pdf) de l’étude annuelle sur le SaaS de la banque Key Bank, menée auprès de 166 entreprises SaaS qui ont un [MRR]({% link indicateurs/monthly-recurring-revenue.md %}) supérieur à 5 millions de $. Dans cette étude, les entreprises interrogées ont un _churn_ médian de 12,6 %.

## Comprendre votre churn avec les cohortes

Le _churn_ client et le _churn_ des revenus sont précieux mais ils comportent une faiblesse : ils mélangent dans un même chiffre des clients différents, qui ont pu décider de résilier leur abonnement à votre service pour des raisons différentes. Un client qui vous a rejoint il y a 3 mois sera comptabilisé de la même manière qu’un de vos plus fidèles clients qui vous a rejoint il y a 5 ans.

Il existe cependant un moyen d’affiner l’analyse de votre churn : l’analyse de cohorte. Cette analyse consiste à regrouper vos clients en fonction d’une caractéristique commune. Le critère qui est souvent utilisé par les entreprises pour affiner l’analyse de leur _churn_ est la date à laquelle leurs clients les ont rejointes. Les clients ainsi regroupés forment des groupes plus homogènes appelés cohortes, sur lesquels vous calculez votre churn. L’analyse de cohorte pourrait par exemple vous montrer que votre taux de _churn_ augmente fortement quelques mois après que vos clients vous rejoignent. Ou que vos clients qui vous ont rejoint il y a 3 ans sont très fidèles, mais que depuis 6 mois, vos nouveaux clients résilient leurs abonnements dans des proportions importantes.

## Pour aller plus loin

- [How to Use Cohort Analysis to Reduce Churn & Improve Retention](https://baremetrics.com/blog/cohort-analysis) (Baremetrics)
