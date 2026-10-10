---
title: "Método Aspose::Words::DocumentBuilder::MoveToSection"
linktitle: "MoveToSection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::MoveToSection. Mueve el cursor al comienzo del cuerpo en una sección especificada en C++."
type: docs
weight: 60000
url: /es/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Mueve el cursor al comienzo del cuerpo en una sección especificada.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sectionIndex | int32_t | El índice de la sección a la que mover. |
## Observaciones


Cuando *sectionIndex* es mayor o igual a 0, especifica un índice desde el comienzo del documento, siendo 0 la primera sección. Cuando *sectionIndex* es menor que 0, especifica un índice desde el final del documento, siendo -1 la última sección.

El cursor se mueve al primer párrafo en el [Body](../../body/) de la sección especificada.

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
