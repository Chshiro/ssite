---
sidebar_position: 3
---

![Map](https://raw.githubusercontent.com/howl111/PlanOfStudy/main/DexeContractsMap.png)

[ParamKeeper.sol](https://github.com/howl111/PlanOfStudy/blob/main/ParamKeeper.md)

 - This contract implements the Manager's address, as well as checks incoming requests for compliance with the allocated roles, is an initializer when logging in.

[PoolLiquidityToken.sol](https://github.com/howl111/PlanOfStudy/blob/main/PoolLiquidityToken.md)

 - This contract synchronizes the pool, initializes it, and uses the mint method to participate in creating a pair of pool tokens.

[BeaconProxy.sol](https://github.com/howl111/PlanOfStudy/blob/main/BeaconProxy.md)

 - This contract implements a proxy that gets the implementation address for each call from a {UpgradeableBeacon}.

[UpgradeableBeacon.sol](https://github.com/howl111/PlanOfStudy/blob/main/UpgradeableBeacon.md)

 - This contract is used in conjunction with one or more instances of {BeaconProxy} to determine their implementation contract, which is where they will delegate all function calls. An owner is able to change the implementation the beacon points to, thus upgrading the proxies that use this beacon.

[TraderPoolFactory.sol](https://github.com/howl111/PlanOfStudy/blob/main/TraderPoolFactory.md)

 - This contract is a factory that initializes the input parameters for a new pool to create it, implementing a pair of tokens and interfaces.

[TraderPool.sol](https://github.com/howl111/PlanOfStudy/blob/main/TraderPool.md)

 - This contract defines pool objects and roles of pool participants, methods for pool management, as well as initialization of subpools for RiskyTokens and delegation of liquidity

[Proxy.sol](https://github.com/howl111/PlanOfStudy/blob/main)

 - This abstract contract provides a fallback function that delegates all calls to another contract using the EVM instruction delegatecall. We refer to the second contract as the implementation behind the proxy, and it has to be specified by overriding the virtual {_implementation} function. Additionally, delegation to the implementation can be triggered manually through the {_fallback} function, or to a different contract through the {_delegate} function. The success and return data of the delegated call will be returned back to the caller of the proxy.
