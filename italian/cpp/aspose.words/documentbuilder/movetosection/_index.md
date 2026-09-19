---
title: "Metodo Aspose::Words::DocumentBuilder::MoveToSection"
linktitle: "MoveToSection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::MoveToSection. Sposta il cursore all'inizio del corpo in una sezione specificata in C++."
type: docs
weight: 60000
url: /it/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Sposta il cursore all'inizio del corpo in una sezione specificata.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sectionIndex | int32_t | L'indice della sezione a cui spostarsi. |
## Note


Quando *sectionIndex* è maggiore o uguale a 0, specifica un indice a partire dall'inizio del documento, con 0 che rappresenta la prima sezione. Quando *sectionIndex* è minore di 0, specifica un indice a partire dalla fine del documento, con -1 che rappresenta l'ultima sezione.

Il cursore viene spostato al primo paragrafo nel [Body](../../body/) della sezione specificata.

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
