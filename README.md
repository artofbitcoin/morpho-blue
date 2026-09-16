# Parcours français

Ce fork propose un parcours documentaire en français consacré à la primitive de prêt Morpho Blue. Le sommaire et les chapitres sont disponibles dans [docs/fr/](./docs/fr/).

# Morpho Blue

Morpho Blue is a non-custodial lending protocol implemented for the Ethereum Virtual Machine.
Morpho Blue offers a new trustless primitive with increased efficiency and flexibility compared to existing lending platforms.
It provides permissionless risk management and permissionless market creation with oracle agnostic pricing.
It also enables higher collateralization factors, improved interest rates, and lower gas consumption.
The protocol is designed to be a simple, immutable, and governance-minimized base layer that allows for a wide variety of other layers to be built on top.
Morpho Blue also offers a convenient developer experience with a singleton implementation, callbacks, free flash loans, and account management features.

## Whitepaper

The protocol is described in detail in the [Morpho Blue Whitepaper](./morpho-blue-whitepaper.pdf).

## Repository Structure

Morpho.sol contains most of the source code of the core contract of Morpho Blue. It solely relies on internal libraries in the src/libraries subdirectory. Libraries in src/libraries/periphery are reusable helpers for integrators. The src/mocks directory contains contracts designed exclusively for testing. Relevant requirements about market dependencies are documented in IMorpho.sol.

## Developers

Compilation, testing and formatting with [forge](https://book.getfoundry.sh/getting-started/installation).

## Audits

All audits are stored in the [audits](./audits/) folder.

## License

Files in this repository are publicly available under license GPL-2.0-or-later, see [LICENSE](./LICENSE).
