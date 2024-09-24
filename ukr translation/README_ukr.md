# Технічна документація Polygon zkEVM

## Загальна інформація
Цей репозиторій містить матеріали документації, що стосуються різних аспектів Polygon zkEVM.
Зокрема, цей репозиторій містить три типи матеріалів:
(A) слайди з описом системи, (B) документи з описом системи (які ми також називаємо шаром знань) і, нарешті, (C) документи з технічними специфікаціями.

## Відмова від відповідальності
Матеріали в цьому репозиторії постійно переглядаються та оновлюються.

## A. Слайди з описом системи

- **Концепції:** [тут](./slides/zkevm-concepts.pdf) ви можете знайти слайди з деякими концепціями, які рекомендується зрозуміти для розуміння zkEVM.
- **Принципи доведення системи:** [тут](./slides/zkevm-architecture-part1-proving-system-principles.pdf) ви можете знайти першу частину слайдів з архітектури zkEVM, що представляють основні принципи системи доведення, яку використовує zkEVM.
- **Секвенціювання та доведення:** [тут](./slides/zkevm-architecture-part2-sequencing-and-proving.pdf) yви можете знайти другу частину слайдів з архітектури zkEVM, де представлені два основні процеси в zkEVM: секвенціювання та доведення.
- **Комунікація між рівнями:** [тут](./slides/zkevm-architecture-part3-layer-communication.pdf) ви можете знайти третю частину слайдів з архітектури zkEVM, яка показує, як різні рівні обмінюються інформацією в архітектурі zkEVM.
- **Обмін активами та повідомленнями:** [тут](./slides/zkevm-architecture-part4-exchanging-assets-and-messages.pdf) и можете знайти четверту частину слайдів з архітектури zkEVM, яка показує, як ми використовуємо обмін між рівнями для передачі активів та повідомлень між рівнями.
- **uLXLY:** [тут](./slides/zkevm-architecture-part5-ulxly.pdf) ви можете знайти п'яту частину слайдів з архітектури zkEVM, що пояснює єдиний LXLY.
- **Економіка:** [тут](./slides/zkevm-architecture-part6-economics.pdf) ви можете знайти шосту частину слайдів з архітектури zkEVM, яка пояснює економічні аспекти zkEVM.

## B. Документи Опису Системи (Шар Знань)

- **Концепції:**
  - [Стан Ethereum](./knowledge-layer/concepts/ethereum-state.pdf)
  - [Шлях до масштабованості](./knowledge-layer/concepts/road-to-scalability.pdf)
  - [Стратегії масштабування L2](./knowledge-layer/concepts/l2-scaling-strategies.pdf)

- **Архітектура:**

  - [Передумови](./knowledge-layer/architecture/pre-requisites.pdf)

  - Принципи доведення системи:

    - [Вступ до системи доведення](./knowledge-layer/architecture/intro-proving-system.pdf)
    - [Концепція дерева станів L2](./knowledge-layer/architecture/l2-state-tree-concept.pdf)
    - [Вхідні дані системи доведення](./knowledge-layer/architecture/proof-inputs.pdf)

  - Секвенціювання та доведення:
    - [Спочатку впорядкувати, потім довести](./knowledge-layer/architecture/order-then-prove.pdf)
    - [Секвенціювання пакетів](./knowledge-layer/architecture/sequencing-batches.pdf)
    - [Агрегатор](./knowledge-layer/architecture/aggregator.pdf)
    - [JSON-RPC](./knowledge-layer/architecture/zkevm-network.pdf)
    - [Дерево станів L2: Ключі та значення](./knowledge-layer/architecture/L2StateTree.pdf)
    - [Обробка блоків L2](./knowledge-layer/architecture/processing-l2-blocks.pdf)
    - [Синхронізатор](./knowledge-layer/architecture/synchronizer.pdf)
  
  - Комунікація між рівнями:

    - [Міст](./knowledge-layer/architecture/bridge.pdf)
    - [Дерево Меркла лише для додавання](./knowledge-layer/architecture/append-only-smt.pdf)
    - [Міст у Etrog](./knowledge-layer/architecture/bridge-etrog.pdf)

  - uLXLY:
    
    - [Єдиний LXLY](./knowledge-layer/architecture/ulxly.pdf)

  - Економіка:

    - [Комісії користувачів](./knowledge-layer/architecture/users-fees.pdf)

- **Специфікації:**
  - [pil-stark](./knowledge-layer/specs/PDFs/estark.pdf)

## C. Документи Технічної Специфікації

Наразі є такі документи (порядок відповідає послідовному читанню):
- [MulMod Opcode](./docs/opcode-mulmod.pdf):
  Цей документ описує реалізацію коду операції mulmod.
- [eSTARK](./docs/estark.pdf):
  Ця стаття описує eAIR, набір обмежень і систему доведення.
- [PIL](./docs/pil.pdf):
  Цей документ описує Мову Ідентичності Поліномів (PIL), яка є новою спеціалізованою мовою, корисною для визначення обмежень eAIR.
- [Proof Recurssion](./docs/proof-recursion.pdf):
  Цей документ визначає, як zkEVM від Polygon доводиться за допомогою рекурсії, агрегації та композиції. Обмеження zkEVM визначаються як поліноміальні ідентичності з використанням мови PIL. Потім, слід виконання можна довести за допомогою специфікації PIL для побудови STARK, який доводиться протоколом FRI. Проблема в тому, що STARK генерує великі докази. Цей документ описує, як використовувати рекурсію разом із композицією для скорочення розміру доказів.