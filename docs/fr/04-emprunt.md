# 4. Emprunt, remboursement et collatéral

Un emprunteur fournit d’abord du collatéral avec `supplyCollateral`. Il peut ensuite appeler `borrow` pour recevoir l’actif de prêt sous la contrainte du LLTV du marché. La dette est également représentée en parts : les intérêts sont intégrés lors de l’actualisation.

`repay` réduit la dette en convertissant les actifs remboursés en parts de dette. Le protocole distingue donc clairement les deux côtés du marché : parts de supply pour les prêteurs, parts de dette pour les emprunteurs.

`accrueInterest` met à jour le taux et les agrégats avant les opérations qui dépendent du temps. Cette étape évite de calculer la solvabilité sur un état périmé et alimente la croissance de la liquidité due aux prêteurs.

Suite : [solvabilité et liquidation](05-liquidation.md).
