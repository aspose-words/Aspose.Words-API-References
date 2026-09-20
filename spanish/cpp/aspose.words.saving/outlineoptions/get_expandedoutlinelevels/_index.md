---
title: "Aspose::Words::Saving::OutlineOptions::get_ExpandedOutlineLevels método"
linktitle: "get_ExpandedOutlineLevels"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OutlineOptions::get_ExpandedOutlineLevels método. Especifica cuántos niveles del esquema del documento se mostrarán expandidos cuando el archivo se visualice en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.saving/outlineoptions/get_expandedoutlinelevels/
---
## OutlineOptions::get_ExpandedOutlineLevels method


Especifica cuántos niveles del esquema del documento se deben mostrar expandidos al visualizar el archivo.

```cpp
int32_t Aspose::Words::Saving::OutlineOptions::get_ExpandedOutlineLevels() const
```

## Observaciones


Tenga en cuenta que estas opciones no funcionarán al guardar en XPS.

Especifique 0 y el esquema del documento se colapsará; especifique 1 y los elementos de primer nivel en el esquema se expandirán y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.
## Ver también

* Class [OutlineOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
