# zkevm-contracts

Реалізація смарт-контракту, який буде використовуватися в Polygon zkEVM

[![Main CI](https://github.com/0xPolygonHermez/zkevm-contracts/actions/workflows/main.yml/badge.svg)](https://github.com/0xPolygonHermez/zkevm-contracts/actions/workflows/main.yml)

## Контракти в мережі Mainnet::

| Contract Name                | Address                                                                                                               |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| PolygonRollupManager         | [0x5132A183E9F3CB7C848b0AAC5Ae0c4f0491B7aB2](https://etherscan.io/address/0x5132A183E9F3CB7C848b0AAC5Ae0c4f0491B7aB2) |
| PolygonZkEVMBridgeV2         | [0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe](https://etherscan.io/address/0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe) |
| PolygonZkEVMGlobalExitRootV2 | [0x580bda1e7A0CFAe92Fa7F6c20A3794F169CE3CFb](https://etherscan.io/address/0x580bda1e7A0CFAe92Fa7F6c20A3794F169CE3CFb) |
| FflonkVerifier               | [0x4F9A0e7FD2Bf6067db6994CF12E4495Df938E6e9](https://etherscan.io/address/0x4F9A0e7FD2Bf6067db6994CF12E4495Df938E6e9) |
| PolygonZkEVMDeployer         | [0xCB19eDdE626906eB1EE52357a27F62dd519608C2](https://etherscan.io/address/0xCB19eDdE626906eB1EE52357a27F62dd519608C2) |
| PolygonZkEVMTimelock         | [0xEf1462451C30Ea7aD8555386226059Fe837CA4EF](https://etherscan.io/address/0xEf1462451C30Ea7aD8555386226059Fe837CA4EF) |

## zkEVM Contracts:

| Contract Name        | Address                                                                                                                        |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| PolygonZkEVMBridgeV2 | [0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe](https://zkevm.polygonscan.com/address/0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe) |
| PolygonZkEVMTimelock | [0xBBa0935Fa93Eb23de7990b47F0D96a8f75766d13](https://zkevm.polygonscan.com/address/0xBBa0935Fa93Eb23de7990b47F0D96a8f75766d13) |

## Вимоги

-   node version: 16.x
-   npm version: 7.x

## Встановлення репозиторію

```
npm i
```

## Запуск тестів

```
npm run test
```

## Деплой на hardhat

```
npm run deploy:ZkEVM:hardhat
```

## Створення Docker контейнерів

```
npm run docker:contracts
```

Або якщо використовуєте нову версію docker-compose

```
npm run dockerv2:contracts
```

Буде створений новий docker `hermeznetwork/geth-zkevm-contracts`
Цей docker міститиме geth ноду з задеплоєними контрактами
Результати деплою можна знайти в: `docker/deploymentOutput/deploy_output.json`
Щоб запустити docker, ви можете використати: `docker run -p 8545:8545 hermeznetwork/geth-zkevm-contracts`

## Примітка

Для тестування використовуються наступні приватні ключі. Ці ключі не призначені для використання в продуктивному середовищі:

-   private key: `0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80`
    -   address:`0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266`
-   private key: `0xdfd01798f92667dbf91df722434e8fbe96af0211d4d1b82bbbbc8f1def7a814f`
    -   address:`0xc949254d682d8c9ad5682521675b8f43b102aec4`

# Перевірка задеплоєних смарт-контрактів

Щоб перевірити, що смарт-контракти з цього репозиторію є тими ж, які задеплоєні на mainnet, ви можете слідувати інструкціям, описаним в [цьому документі](verifyMainnetDeployment/verifyDeployment.md)

Смарт-контракт, який використовується для верифікації доказів, є згенерованим контрактом з zkEVM Rom та Pil (обмеження). Щоб перевірити деплой цього смарт-контракту, ви можете слідувати інструкціям, описаним в [цьому документі](verifyMainnetDeployment/verifyMainnetProofVerifier.md)

## Активація github hook

```
git config --local core.hooksPath .githooks/
```
