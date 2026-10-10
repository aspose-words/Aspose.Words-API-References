---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock método"
linktitle: "GetBuildingBlock"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock método. Encuentra un bloque de construcción usando la galería, categoría y nombre especificados en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Busca un building block usando la galería, categoría y nombre especificados.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| galería | Aspose::Words::BuildingBlocks::BuildingBlockGallery | Los criterios de la galería. |
| categoría | const System::String\& | Los criterios de la categoría. Puede ser **null**, en cuyo caso no se utilizará para la comparación. |
| name | const System::String\& | Los criterios del nombre del bloque de construcción. |

### ReturnValue

El bloque de construcción coincidente o **null** si no se encontró una coincidencia.
## Observaciones


Este es un método de conveniencia que itera sobre todos los bloques de construcción en esta colección y devuelve el primer bloque de construcción que coincide con la galería, categoría y nombre especificados.

Microsoft Word organiza los bloques de construcción en galerías. Las galerías están predefinidas usando el enumerado [BuildingBlockGallery](../../buildingblockgallery/). Dentro de cada galería, los bloques de construcción pueden organizarse en una o más categorías. El nombre de la categoría es una cadena. Cada bloque de construcción tiene un nombre. No se garantiza que el nombre de un bloque de construcción sea único.

## Ver también

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
