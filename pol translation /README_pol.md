# Repozytorium Dokumentacji Technicznej Polygon zkEVM

## Informacje Ogólne
To repozytorium zawiera materiały dokumentacyjne dotyczące różnych aspektów Polygon zkEVM. W szczególności, repozytorium zawiera trzy rodzaje materiałów: (A) slajdy z opisem systemu, (B) dokumenty opisujące system (które nazywamy również naszą warstwą wiedzy) oraz (C) dokumenty specyfikacji technicznej.

## Zastrzeżenie
Materiały w tym repozytorium są ciągle przeglądane i aktualizowane.

## A. Slajdy z Opisem Systemu

- **Koncepcje:** [tutaj](./slides/zkevm-concepts.pdf) można znaleźć slajdy dotyczące niektórych koncepcji, które są zalecane do zrozumienia zkEVM. 
- **Zasady Systemu Dowodzenia:** [tutaj](./slides/zkevm-architecture-part1-proving-system-principles.pdf) można znaleźć pierwszą część slajdów dotyczących architektury zkEVM, która przedstawia podstawowe zasady systemu dowodzenia wykorzystywanego przez zkEVM.
- **Sekwencjonowanie i Dowodzeni:** [tutaj](./slides/zkevm-architecture-part2-sequencing-and-proving.pdf) można znaleźć drugą część slajdów dotyczących architektury zkEVM, która przedstawia dwa główne procesy w zkEVM: sekwencjonowanie i dowodzenie.
- **Komunikacja Między Warstwami:** [tutaj](./slides/zkevm-architecture-part3-layer-communication.pdf) można znaleźć trzecią część slajdów dotyczących architektury zkEVM, która pokazuje, jak różne warstwy wymieniają informacje w architekturze zkEVM.
- **Wymiana Aktywów i Wiadomości:** [tutaj](./slides/zkevm-architecture-part4-exchanging-assets-and-messages.pdf) można znaleźć czwartą część slajdów dotyczących architektury zkEVM, która pokazuje, jak wykorzystujemy wymianę warstw do transferu aktywów i wiadomości między warstwami.
- **uLXLY:** [tutaj](./slides/zkevm-architecture-part5-ulxly.pdf) można znaleźć piątą część slajdów dotyczących architektury zkEVM, która wyjaśnia zjednoczone LXLY.
- **Ekonomia:** [tutaj](./slides/zkevm-architecture-part6-economics.pdf) można znaleźć szóstą część slajdów dotyczących architektury zkEVM, która wyjaśnia aspekty ekonomiczne zkEVM.

## B. Dokumenty Opisujące System (Warstwa Wiedzy)

- **Koncepcje:**
  - [Stan Ethereum](./knowledge-layer/concepts/ethereum-state.pdf)
  - [Droga do Skalowalności](./knowledge-layer/concepts/road-to-scalability.pdf)
  - [Strategie Skalowania L2](./knowledge-layer/concepts/l2-scaling-strategies.pdf)

- **Architektura:**

  - [Wymagania Wstępne](./knowledge-layer/architecture/pre-requisites.pdf)

  - Zasady Systemu Dowodzenia:

    - [Wprowadzenie do Systemu Dowodzenia](./knowledge-layer/architecture/intro-proving-system.pdf)
    - [Koncepcja Drzewa Stanów L2](./knowledge-layer/architecture/l2-state-tree-concept.pdf)
    - [Wejścia Systemu Dowodzenia](./knowledge-layer/architecture/proof-inputs.pdf)

  - Sekwencjonowanie i Dowodzenie:
    - [Najpierw Kolejność, Potem Dowodzenie](./knowledge-layer/architecture/order-then-prove.pdf)
    - [Sekwencjonowanie Pakietów](./knowledge-layer/architecture/sequencing-batches.pdf)
    - [Agregator](./knowledge-layer/architecture/aggregator.pdf)
    - [JSON-RPC](./knowledge-layer/architecture/zkevm-network.pdf)
    - [L2StateTree: Klucze i Wartości](./knowledge-layer/architecture/L2StateTree.pdf)
    - [Przetwarzanie Bloków L2](./knowledge-layer/architecture/processing-l2-blocks.pdf)
    - [Synchronizator](./knowledge-layer/architecture/synchronizer.pdf)
  
  - Komunikacja Między Warstwami:
    - [Most](./knowledge-layer/architecture/bridge.pdf)
    - [Dodaj Tylko Drzewo Merkle](./knowledge-layer/architecture/append-only-smt.pdf)
    - [Most w Etrog](./knowledge-layer/architecture/bridge-etrog.pdf)

  - uLXLY:
    
    - [Zjednoczone LXLY](./knowledge-layer/architecture/ulxly.pdf)

  - Ekonomia:

    - [Opłaty Użytkowników](./knowledge-layer/architecture/users-fees.pdf)

- **Specyfikacje:**
  - [pil-stark](./knowledge-layer/specs/PDFs/estark.pdf)

## C. Dokumenty Specyfikacji Technicznej

Obecnie dostępne są następujące dokumenty (kolejność jest ważna dla linearnego czytania):
- [MulMod Opcode](./docs/opcode-mulmod.pdf):
  Ten dokument opisuje implementację opcode'u mulmod.
- [eSTARK](./docs/estark.pdf):
  Ten dokument opisuje eAIR, zestaw ograniczeń i jego system dowodzenia.
- [PIL](./docs/pil.pdf):
  Ten dokument opisuje Język Tożsamości Wielomianowej (PIL), który jest nowym językiem specyficznym dla domeny, użytecznym do definiowania ograniczeń eAIR.
- [Proof Recurssion](./docs/proof-recursion.pdf):
  Ten dokument opisuje, jak polygon zkEVM jest dowodzony za pomocą rekurencji, agregacji i kompozycji. Ograniczenia zkEVM są określone jako tożsamości wielomianowe za pomocą języka PIL. Następnie ślad wykonania może być dowodzony za pomocą specyfikacji PIL do budowy STARK, który jest dowodzony za pomocą protokołu FRI. Problem polega na tym, że STARKi generują duże dowody. Ten dokument opisuje, jak wykorzystać rekurencję razem z kompozycją, aby skrócić rozmiar dowodu.