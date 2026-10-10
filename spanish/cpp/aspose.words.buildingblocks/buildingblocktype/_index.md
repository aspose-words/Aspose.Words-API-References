---
title: "Aspose::Words::BuildingBlocks::BuildingBlockType enum"
linktitle: "BuildingBlockType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockType enum. Especifica un tipo de bloque de construcción. El tipo podría afectar la visibilidad y el comportamiento del bloque de construcción en Microsoft Word en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enum


Especifica un tipo de bloque de construcción. El tipo podría afectar la visibilidad y el comportamiento del bloque de construcción en Microsoft Word.

```cpp
enum class BuildingBlockType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se especifica información de tipo para el bloque de construcción. |
| AutomaticallyReplaceNameWithContent | 1 | Permite que el bloque de construcción se inserte automáticamente en el documento siempre que su nombre se introduzca en una aplicación. |
| StructuredDocumentTagPlaceholderText | 2 | El bloque de construcción es un texto de marcador de posición de etiqueta de documento estructurado. |
| FormFieldHelpText | 3 | El bloque de construcción es un texto de ayuda de campo de formulario. |
| Normal | 4 | El bloque de construcción es una entrada normal (es decir, regular) del documento de glosario. |
| AutoCorrect | 5 | El bloque de construcción está asociado con las herramientas de ortografía y gramática. |
| AutoText | 6 | El bloque de construcción es una entrada de AutoText. |
| Todo | 7 | El bloque de construcción está asociado con todos los tipos. |
| Default | n/a | Guardar como [None](./). |

## Observaciones


Corresponde al tipo **ST_DocPartType** en OOXML.

## Ver también

* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
