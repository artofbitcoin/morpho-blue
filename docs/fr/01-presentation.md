# 1. Le rôle de Morpho Blue

Morpho Blue est un protocole de prêt non custodial pour l’EVM. Son contrat central propose une primitive volontairement compacte : des marchés isolés, créés sans permission, où les paramètres de risque sont explicites et où les utilisateurs conservent la maîtrise de leurs actifs.

Le dépôt présente `src/Morpho.sol` comme le cœur du protocole. Les bibliothèques internes encadrent les calculs de parts, les transferts sûrs, les erreurs et les événements. Les intégrateurs peuvent ensuite construire des couches de risque, des interfaces et des stratégies au-dessus de cette base.

La conception privilégie l’immutabilité et une gouvernance minimale. En contrepartie, chaque marché doit être compris séparément : l’oracle, le modèle de taux et le seuil de liquidation font partie de son identité.

Suite : [les paramètres d’un marché](02-marche.md).
