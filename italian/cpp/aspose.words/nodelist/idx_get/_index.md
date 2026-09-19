---
title: "Aspose::Words::NodeList::idx_get method"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NodeList::idx_get method. Recupera un nodo all'indice specificato in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Recupera un nodo all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella lista dei nodi. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Vedi anche

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
