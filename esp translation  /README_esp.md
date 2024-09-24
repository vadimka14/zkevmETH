# Repositorio de Documentación Técnica de Polygon zkEVM

## Información General
Este repositorio contiene material de documentación sobre los diferentes aspectos de Polygon zkEVM.
En particular, este repositorio contiene tres tipos de materiales:
(A) diapositivas de descripción del sistema, (B) documentos de descripción del sistema (que también llamamos nuestra capa de conocimiento) y finalmente, (C) documentos de especificación técnica.

## Descargo de Responsabilidad
Los materiales en este repositorio están siendo revisados y actualizados continuamente.

## A. Diapositivas de Descripción del Sistema

- **Conceptos:** [Aquí](./slides/zkevm-concepts.pdf) puedes encontrar diapositivas sobre algunos conceptos recomendados para entender el zkEVM. 
- **Principios del Sistema de Pruebas:** [Aquí](./slides/zkevm-architecture-part1-proving-system-principles.pdf) puedes encontrar la primera parte de las diapositivas de la arquitectura zkEVM que presentan los principios básicos del sistema de pruebas utilizado por el zkEVM.
- **Secuenciación y Pruebas:** [Aquí](./slides/zkevm-architecture-part2-sequencing-and-proving.pdf) puedes encontrar la segunda parte de las diapositivas de la arquitectura zkEVM que presentan los dos procesos principales en el zkEVM: la secuenciación y las pruebas.
- **Comunicación entre Capas:** [Aquí](./slides/zkevm-architecture-part3-layer-communication.pdf) puedes encontrar la tercera parte de las diapositivas de la arquitectura zkEVM que muestra cómo las diferentes capas intercambian información en la arquitectura zkEVM.
- **Intercambio de Activos y Mensajes:** [Aquí](./slides/zkevm-architecture-part4-exchanging-assets-and-messages.pdf) puedes encontrar la cuarta parte de las diapositivas de la arquitectura zkEVM que muestra cómo utilizamos el intercambio de capas para transferir activos y mensajes entre capas.
- **uLXLY:** [Aquí](./slides/zkevm-architecture-part5-ulxly.pdf) puedes encontrar la quinta parte de las diapositivas de la arquitectura zkEVM que explica el LXLY unificado. 
- **Economía:** [Aquí](./slides/zkevm-architecture-part6-economics.pdf) puedes encontrar la sexta parte de las diapositivas de la arquitectura zkEVM que explica los aspectos económicos del zkEVM.

## B. Documentos de Descripción del Sistema (Capa de Conocimiento)

- **Conceptos:**
  - [Estado de Ethereum](./knowledge-layer/concepts/ethereum-state.pdf)
  - [Camino hacia la Escalabilidad](./knowledge-layer/concepts/road-to-scalability.pdf)
  - [Estrategias de Escalado L2](./knowledge-layer/concepts/l2-scaling-strategies.pdf)

- **Arquitectura:**

  - [Requisitos Previos](./knowledge-layer/architecture/pre-requisites.pdf)

  - Principios del Sistema de Pruebas:
    - [Introducción al Sistema de Pruebas](./knowledge-layer/architecture/intro-proving-system.pdf)
    - [Concepto del Árbol de Estado L2](./knowledge-layer/architecture/l2-state-tree-concept.pdf)
    - [Entradas del Sistema de Pruebas](./knowledge-layer/architecture/proof-inputs.pdf)

  - Secuenciación y Pruebas:
    - [Ordenar y Luego Probar](./knowledge-layer/architecture/order-then-prove.pdf)
    - [Secuenciación de Lotes](./knowledge-layer/architecture/sequencing-batches.pdf)
    - [Agregador](./knowledge-layer/architecture/aggregator.pdf)
    - [JSON-RPC](./knowledge-layer/architecture/zkevm-network.pdf)
    - [L2StateTree: Claves y Valores](./knowledge-layer/architecture/L2StateTree.pdf)
    - [Procesamiento de Bloques L2](./knowledge-layer/architecture/processing-l2-blocks.pdf)
    - [Sincronizador](./knowledge-layer/architecture/synchronizer.pdf)
  
  - Comunicación entre Capas:

    - [Puente](./knowledge-layer/architecture/bridge.pdf)
    - [Árbol de Merkle Solo de Adición](./knowledge-layer/architecture/append-only-smt.pdf)
    - [Puente en Etrog](./knowledge-layer/architecture/bridge-etrog.pdf)

  - uLXLY:
    
    - [LXLY Unificado](./knowledge-layer/architecture/ulxly.pdf)

  - Economía:

    - [Tarifas de Usuarios](./knowledge-layer/architecture/users-fees.pdf)

- **Especificaciones:**
  - [pil-stark](./knowledge-layer/specs/PDFs/estark.pdf)

## C. Documentos de Especificación Técnica

Actualmente hay los siguientes documentos (el orden es válido para lectura lineal):
- [MulMod Opcode](./docs/opcode-mulmod.pdf):
  Este documento describe la implementación del opcode mulmod.
- [eSTARK](./docs/estark.pdf):
  Este documento describe eAIR, un conjunto de restricciones y su sistema de pruebas.
- [PIL](./docs/pil.pdf):
  Este documento describe el Lenguaje de Identidad Polinómica (PIL), que es un lenguaje específico de dominio útil para definir las restricciones eAIR.
- [Proof Recurssion](./docs/proof-recursion.pdf):
  Este documento especifica cómo se prueba el polygon zkEVM utilizando recursión, agregación y composición. Las restricciones del zkEVM se especifican como identidades polinómicas utilizando el lenguaje PIL. Luego, una traza de ejecución puede ser probada utilizando la especificación PIL para construir un STARK que se prueba con el protocolo FRI. El problema es que los STARKs generan pruebas grandes. Este documento describe cómo usar la recursión junto con la composición para reducir el tamaño de la prueba.
