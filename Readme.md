# General Idea :

L’idée dans le chantier 2 est de détecter les foyers potentiels avant leurs propagations, ainsi que catégoriser le risque d’une région. Elle va servir dans la détection prédictive de foyers pour employer des tests massifs avant plus de propagation, ainsi que de comprendre les différents besoins de chaque région.

## Inputs :

- Les données nécessaires pour celà qui seront prises en input : 
- Les scores de risque (chantier 1) de chaque personne détectée contaminée
- Les dernières localisations de 14 jours de la personne contaminée 
- Les scores de risque des personnes à risque d’infection (qui ont rencontrés les personnes contaminées).
- Les dernières localisations de 14 jours de la personne à risque.
- Densité de la population pour les zones. 

## Constraints :

Nous devons pourtant tenir en compte que compter les personnes à risque va donner des zones de risques très massives, et faire exploser les scores de risques des zones, vu le grand nombre potentiel des personnes à risque d’infection, surtout dans le futur. Ca donnera plus exactement un grand nombre de faux positifs, qui sera peut être difficilement gérable par les autorités en cas d’explosions de cas car ça augmente trop les scores de risque des zones.
Un coefficient faible devrait alors être donné aux personnes à risque d’infection, pour éviter plusieurs faux positifs dans les zones à risques. Ce coefficient devra pourtant changer dans le temps, selon la période et ses conditions, ainsi que la prévalence de détections de cas.

Un coefficient initial pour le lancement de l’application est .7 pour les personnes à risque, comparés un coeff de 1. Pour les personnes contaminées. Ce coefficient sera testé pour voir le taux des faux positifs. Il est à noter que nous travaillerons avec ce coefficient dans les zones à faibles prévalence de la maladie.
Ces coefficients devront être révisés en Septembre avec les nouvelles conditions du temps (plus de potentiel cas dans cette période, donc il devra être rabaissé).

Pour la granularité, dans le cas de détection des foyers à travers les zones à risques, la plus petite granularité significative est recommandée. Un cercle de rayon de 100m est trop petit, et de rayon de 500m est trop grand. Ce point devra être présenté au gouvernement pour qu’ils choisissent eux même ce qu’ils considèrent comme la taille la plus significative pour eux.

Pour la granularité, dans le cas de catégorisation des actions à mener pour chaque région, une granularité par commune autour d’un hôpital pourrait peut être pertinente.

## Contributions : 

Please check the `TODOs` file and see if you can work on any task there.

If you will, please do it in a separate branch for that specific task, and then make a pull request !
