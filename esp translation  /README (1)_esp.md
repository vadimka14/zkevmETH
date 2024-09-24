# zkevm-contracts

Implementación de contratos inteligentes que serán utilizados por el Polygon zkEVM

[![Main CI](https://github.com/0xPolygonHermez/zkevm-contracts/actions/workflows/main.yml/badge.svg)](https://github.com/0xPolygonHermez/zkevm-contracts/actions/workflows/main.yml)

## Contratos en Mainnet:

| Contract Name                | Address                                                                                                               |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| PolygonRollupManager         | [0x5132A183E9F3CB7C848b0AAC5Ae0c4f0491B7aB2](https://etherscan.io/address/0x5132A183E9F3CB7C848b0AAC5Ae0c4f0491B7aB2) |
| PolygonZkEVMBridgeV2         | [0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe](https://etherscan.io/address/0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe) |
| PolygonZkEVMGlobalExitRootV2 | [0x580bda1e7A0CFAe92Fa7F6c20A3794F169CE3CFb](https://etherscan.io/address/0x580bda1e7A0CFAe92Fa7F6c20A3794F169CE3CFb) |
| FflonkVerifier               | [0x4F9A0e7FD2Bf6067db6994CF12E4495Df938E6e9](https://etherscan.io/address/0x4F9A0e7FD2Bf6067db6994CF12E4495Df938E6e9) |
| PolygonZkEVMDeployer         | [0xCB19eDdE626906eB1EE52357a27F62dd519608C2](https://etherscan.io/address/0xCB19eDdE626906eB1EE52357a27F62dd519608C2) |
| PolygonZkEVMTimelock         | [0xEf1462451C30Ea7aD8555386226059Fe837CA4EF](https://etherscan.io/address/0xEf1462451C30Ea7aD8555386226059Fe837CA4EF) |

## Contratos zkEVM:

| Contract Name        | Address                                                                                                                        |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| PolygonZkEVMBridgeV2 | [0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe](https://zkevm.polygonscan.com/address/0x2a3DD3EB832aF982ec71669E178424b10Dca2EDe) |
| PolygonZkEVMTimelock | [0xBBa0935Fa93Eb23de7990b47F0D96a8f75766d13](https://zkevm.polygonscan.com/address/0xBBa0935Fa93Eb23de7990b47F0D96a8f75766d13) |

## Requisitos

-   node version: 16.x
-   npm version: 7.x

## Instalar repositorio

```
npm i
```

## Ejecutar pruebas

```
npm run test
```

## Desplegar en Hardhat

```
npm run deploy:ZkEVM:hardhat
```

## Construir Dockers

```
npm run docker:contracts
```

O si usas la nueva versión de docker-compose

```
npm run dockerv2:contracts
```

Se creará un nuevo docker `hermeznetwork/geth-zkevm-contracts`
Este docker contendrá un nodo geth con los contratos desplegados
La salida del despliegue se puede encontrar en: `docker/deploymentOutput/deploy_output.json`
Para ejecutar el docker, puedes usar: `docker run -p 8545:8545 hermeznetwork/geth-zkevm-contracts`

## Nota

Para probar, se están utilizando las siguientes claves privadas. Estas claves no están destinadas a ser usadas en ningún entorno de producción:

-   private key: `0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80`
    -   address:`0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266`
-   private key: `0xdfd01798f92667dbf91df722434e8fbe96af0211d4d1b82bbbbc8f1def7a814f`
    -   address:`0xc949254d682d8c9ad5682521675b8f43b102aec4`

# Verificar Contratos Inteligentes Desplegados

Para verificar que los contratos inteligentes de este repositorio son los mismos que se han desplegado en la mainnet, puedes seguir las instrucciones descritas en el [documento](verifyMainnetDeployment/verifyDeployment.md)

El contrato inteligente utilizado para verificar una prueba es un contrato generado a partir del zkEVM Rom y Pil (restricciones). Para verificar el despliegue de este contrato inteligente, puedes seguir las instrucciones descritas en este [documento](verifyMainnetDeployment/verifyMainnetProofVerifier.md)

## Activar el hook de GitHub

```
git config --local core.hooksPath .githooks/
```
