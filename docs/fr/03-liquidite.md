# 3. Dépôts, retraits et parts

Les fournisseurs de liquidité utilisent `supply` pour déposer l’actif prêté et recevoir des parts de supply. Le protocole conserve un nombre de parts plutôt qu’un solde individuel en actifs : la valeur d’une part évolue avec les intérêts et les pertes réalisées.

`withdraw` inverse ce mécanisme en brûlant les parts demandées et en transférant les actifs correspondants. Les conversions passent par `SharesMathLib` afin de limiter les arrondis favorables à un appelant et de préserver les invariants du marché.

Le contrat central effectue les transferts via `SafeTransferLib`. Les callbacks permettent à un intégrateur de composer une opération atomique, mais ils élargissent aussi la surface d’analyse : l’état et les autorisations doivent être vérifiés à chaque étape.

Suite : [emprunter et rembourser](04-emprunt.md).
