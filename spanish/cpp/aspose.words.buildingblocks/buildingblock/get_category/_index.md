---
title: "Método Aspose::Words::BuildingBlocks::BuildingBlock::get_Category"
linktitle: "get_Category"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BuildingBlocks::BuildingBlock::get_Category. Especifica la categorización de segundo nivel para el bloque de construcción en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.buildingblocks/buildingblock/get_category/
---
## BuildingBlock::get_Category method


Especifica la categorización de segundo nivel para el bloque de construcción.

```cpp
System::String Aspose::Words::BuildingBlocks::BuildingBlock::get_Category() const
```

## Observaciones


Los bloques de construcción en la interfaz de usuario de Microsoft Word se organizan en galerías. Cada [Gallery](../get_gallery/) puede tener múltiples categorías. Cada bloque dentro de una [Category](./) tiene un [Name](../get_name/).

No puede ser **null** y no puede ser una cadena vacía.

Corresponde al elemento **docPartPr.category.name** en OOXML.

## Ver también

* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
