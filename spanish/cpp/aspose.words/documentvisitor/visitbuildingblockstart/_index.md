---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart método"
linktitle: "VisitBuildingBlockStart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart método. Se llama cuando la enumeración de un bloque de construcción ha comenzado en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor::VisitBuildingBlockStart method


Se llama cuando la enumeración de un bloque de construcción ha comenzado.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockStart(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bloque | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | El objeto que está siendo visitado. |

### ReturnValue

Un valor [VisitorAction](../../visitoraction/) que especifica cómo continuar la enumeración.
## Observaciones


Nota: Un nodo de bloque de construcción y sus hijos no son visitados cuando ejecutas un Visitor sobre un [Document](../../document/). Si deseas ejecutar un Visitor sobre un bloque de construcción, necesitas ejecutar el visitor sobre [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) o llamar a [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## Ver también

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
