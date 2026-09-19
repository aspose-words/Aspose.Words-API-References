---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get metodo. Recupera un blocco di costruzione all'indice specificato in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.buildingblocks/buildingblockcollection/idx_get/
---
## BuildingBlockCollection::idx_get method


Recupera un blocco di costruzione all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella lista dei blocchi di costruzione. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Vedi anche

* Class [BuildingBlock](../../buildingblock/)
* Class [BuildingBlockCollection](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
