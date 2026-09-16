# 5. Solvabilité et liquidation

La liquidation intervient lorsqu’une dette dépasse la valeur de collatéral autorisée par le LLTV, après prise en compte du prix fourni par l’oracle. Un liquidateur rembourse tout ou partie de la dette et reçoit en échange une quantité de collatéral calculée par le protocole.

`liquidate` limite la saisie à la dette effectivement remboursée et applique le bonus prévu par le marché. Le calcul doit conserver les arrondis et les plafonds afin d’éviter qu’une liquidation ne crée une créance supplémentaire ou ne retire plus de collatéral que nécessaire.

Les callbacks et les flash loans rendent possibles des liquidations composables en une transaction. Ils ne suppriment pas le besoin de vérifier les soldes, les parts et les autorisations : ils déplacent une partie de la logique vers l’appelant.

Suite : [limites et périmètre](06-limites.md).
