---
layout: default
title: LTV
description: Découvrez comment calculer votre customer lifetime value (LTV).
image: /assets/images/cards/card-indicateurs-customer-lifetime-value.png
parent: Indicateurs
---

# La Customer lifetime value (LTV)

La _Customer lifetime value_, ou « valeur vie client » en français, est un indicateur qui mesure le revenu moyen que générera l’un de vos clients, pendant le temps qu’il sera votre client. Nous abrégerons dans cet article la Customer Lifetime Value en « LTV » — vous la trouverez aussi ailleurs sous les acronymes CLV, ou CLTV.

## Deux types de LTV

Vous pouvez calculer deux types de Customer Lifetime Value :

- Une LTV « historique », calculée à partir des revenus _réellement_ générés par vos clients. Cette LTV historique mesure le revenu total que vous a fait gagner un client, jusqu’ici. Vous pouvez la calculer pour un client donné, ou calculer une moyenne de LTV historique.
- Une LTV « prédictive », qui mesure le revenu que chacun de vos clients générera en moyenne dans le futur. C’est cette LTV, la plus adoptée par les entreprises innovantes, qui nous intéressera principalement dans le cadre de cet article.

## La Customer Lifetime Value historique

La LTV historique mesure le revenu généré par vos clients jusqu’au moment où vous calculez la LTV. Vous pouvez calculer la LTV de clients qui ne sont plus vos clients, et des clients qui sont toujours vos clients — dans ce cas, la LTV que vous calculerez sera sous-estimée, puisque le calcul n’inclura pas les revenus futurs que vos clients actuels vous feront gagner.

Calculer la LTV historique d’un client donné revient simplement à sommer l’ensemble des revenus générés par ce client :

```
LTV (client A) = Somme des revenus générés par le client
```

Si vous souhaitez calculer votre LTV historique moyenne, divisez simplement l’ensemble des revenus générés par vos clients jusqu’ici, par le nombre de clients que vous avez eus depuis la création de votre entreprise :

```
LTV (moyenne) = Revenus / Nombre de clients
```

#### Exemple de calcul

Vous êtes le dirigeant d’une entreprise innovante qui existe depuis 3 ans. Vous souhaitez calculer votre LTV historique depuis la création de votre entreprise.

Depuis votre création, vous avez dégagé 315 000 € de revenus, et avez, ou avez eu, 90 clients.

Votre LTV historique est :

```
LTV (historique) = 315 000 € / 90 = 3 500 €
```

## La Customer Lifetime Value prédictive

La Customer Lifetime Value dite « prédictive » s’intéresse au montant moyen de nouveau revenu que chacun de vos clients générera, du moment où votre client devient votre client jusqu’au moment où il cesse de l’être — ou au montant de revenu que chaque nouveau client qui vous rejoint générera. Contrairement à la LTV historique, la LTV prédictive intègre donc également les revenus futurs (théoriques) de vos clients.

L’un des principaux intérêts de la LTV prédictive est de vous permettre de vous rendre compte si le coût que vous payez pour attirer vos nouveaux clients est justifié : si vous dépensez plus pour conquérir un client, que ce que ce client vous apportera tout au long de sa relation commerciale avec vous, vous avez un problème.

La LTV prédictive peut se calculer de différentes manières, plus ou moins complexes. Certains modèles de LTV prédictive sont fondés sur des modèles statistiques, ou intègrent des algorithmes de science des données. Le modèle de LTV prédictive que nous vous proposons ici est un modèle simple, adopté par de nombreuses entreprises innovantes. Revers de cette simplicité, ce modèle est une approximation de votre LTV prédictive qui peut être assez volatile, notamment si votre [churn]({% link indicateurs/churn.md %}) varie fortement de mois en mois.

La LTV prédictive se calcule comme suit :

```
LTV = ARPU / Churn
```

Où :

- L’ARPU désigne le revenu moyen par utilisateur, sur une période donnée. La formule de calcul de l’ARPU est : ARPU = (Revenu total sur une période donnée) / (Nombre d’utilisateurs sur cette période). Si vous êtes une entreprise SaaS, calculez votre ARPU d’après votre revenu récurrent, comme votre MRR : ARPU (mois donné) = (MRR sur le mois donné) / (Nombre d’utilisateurs sur le mois donné.)
- Le churn client mesure la perte de vos clients sur une période donnée. Ce churn est un pourcentage, résultat du rapport entre le nombre de clients que vous perdez sur la période choisie (un mois, un trimestre, une année), et le nombre de clients que vous aviez au début de cette période.

#### Exemple de calcul

Vous dirigez une entreprise SaaS, et souhaitez calculer la LTV de vos clients. Vous avez au 31 mars 100 clients : 50 de vos clients sont abonnés à votre formule Simple à 50 € par mois, et 50 de vos clients sont abonnés à votre formule Premium à 100 € par mois.

Pendant le mois de mars, vous avez subi un [churn]({% link indicateurs/churn.md %}) client de 3 %.

Nous avons donc :

```
MRR (mars) = 50 × 50 € + 50 × 100 € = 7 500 €
ARPU (mars) = MRR / Nombre de clients sur le mois = 7 500 / 100 = 75 €
LTV = ARPU / Churn = 75 € / 3 % = 2 500 €
```

Vous pouvez vous attendre à ce que les clients qui sont les vôtres au mois de mars vous apportent dans le futur un revenu de 2 500 €.

### Limites de l’indicateur

Cette formule de calcul de la LTV est simple et efficace, mais elle doit être considérée comme une estimation de votre LTV réelle. Si vous êtes une jeune entreprise innovante, votre [churn]({% link indicateurs/churn.md %}) varie probablement de façon significative chaque mois, ce qui ne signifie pas forcément que votre LTV diminue ou augmente dans les mêmes proportions.

Par ailleurs, la LTV que vous calculez à une date T sur la base de vos clients existants ne prend pas en compte les évolutions de prix que vous pourriez décider au cours des prochains mois, ou les fonctionnalités payantes qui pourraient être adoptées par les clients à partir desquels vous calculez votre LTV.

#### Exemple de calcul

Reprenons notre exemple précédent : vous avez subi au mois de mars un [churn]({% link indicateurs/churn.md %}) de 3 %. Imaginons que le mois suivant, votre [churn]({% link indicateurs/churn.md %}) passe à 5 %. Pour un même nombre de clients, votre nouvelle LTV devient : LTV = 75 € / 5 % = 1 500 €, au lieu de 2 500 €. Votre LTV a baissé théoriquement de 40 %. En réalité, il est probable que votre LTV n’ait pas autant baissé pour l’instant. Vous devez la calculer de mois en mois et suivre son évolution sur le long terme.

## Utilité de l’indicateur

### Comparer LTV et coût d’acquisition client (CAC)

L’intérêt de la LTV réside principalement dans sa comparaison avec votre [coût d’acquisition client]({% link indicateurs/cout-acquisition-client.md %}), ou « CAC ». Votre CAC mesure l’ensemble des dépenses que vous engagez pour attirer un client. Si votre CAC moyen est supérieur à votre LTV moyenne, cela signifie que vous dépensez plus d’argent pour conquérir un nouveau client, que ce nouveau client ne générera de revenu. Vous avez donc un gros problème : chaque nouveau client vous fait en réalité perdre de l’argent. Vous pouvez comparer la LTV à votre CAC en utilisant le [ratio LTV/CAC]({% link indicateurs/ratio-ltv-cac.md %}).

### Identifier vos clients les plus importants

Votre objectif en tant qu’entreprise innovante est d’augmenter la LTV de vos clients, c’est-à-dire de ne pas faire reposer votre croissance uniquement sur l’acquisition de nouveaux clients, mais sur la fidélisation de vos clients existants.

La LTV que vous calculez grâce à la formule décrite ci-dessus est une LTV moyenne : en réalité, tous vos clients ont une LTV différente, tous vos clients généreront un revenu différent au cours de leur vie de client. Parmi vos clients, il est important que vous identifiiez ceux qui ont une LTV supérieure, afin de comprendre pourquoi ils dépensent plus, et de corriger votre modèle : revoir votre _pricing_, mieux communiquer sur certaines fonctionnalités, améliorer votre service client, etc.

Pour effectuer cette analyse, vous devez créer des cohortes de clients, c’est-à-dire regrouper vos clients en fonction d’une caractéristique commune, et calculer les LTV de ces cohortes. C’est le même processus que vous utilisez peut-être pour comparer votre [churn]({% link indicateurs/churn.md %}) auprès de différents profils de clients. Vous pouvez créer vos cohortes de clients en fonction des critères suivants :

- la date à laquelle vos clients vous ont rejoint (en général le mois ou le trimestre) ;
- la formule d’abonnement choisie, si vous êtes une entreprise SaaS ;
- la souscription à des fonctionnalités payantes.
