# 2. L’identité d’un marché

Morpho Blue ne regroupe pas tous les actifs dans un pool universel. Un marché est défini par une structure de paramètres : actif de prêt, actif de collatéral, oracle, modèle de taux d’intérêt et facteur de liquidation. La bibliothèque `MarketParamsLib` calcule l’identifiant déterministe à partir de cette structure.

`createMarket` enregistre un marché une seule fois. Cette séparation rend le risque lisible : modifier l’oracle ou le seuil ne revient pas à changer discrètement un pool existant, mais à sélectionner un autre ensemble de paramètres.

Le modèle de taux est appelé pour actualiser l’état du marché. L’oracle fournit le prix utilisé pour comparer la dette au collatéral, tandis que le LLTV fixe la limite de solvabilité. La qualité de ces dépendances conditionne directement la sécurité économique.

Suite : [les dépôts et les retraits](03-liquidite.md).
