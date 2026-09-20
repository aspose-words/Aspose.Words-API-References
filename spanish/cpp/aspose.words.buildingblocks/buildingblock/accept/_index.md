---
title: "Método Aspose::Words::BuildingBlocks::BuildingBlock::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BuildingBlocks::BuildingBlock::Accept. Acepta un visitante en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará los nodos. |

### ReturnValue

Verdadero si se visitaron todos los nodos; falso si [DocumentVisitor](../../../aspose.words/documentvisitor/) detuvo la operación antes de visitar todos los nodos.
## Observaciones


Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en [DocumentVisitor](../../../aspose.words/documentvisitor/).

Para más información, consulte el patrón de diseño Visitor.

Llama a [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/), luego llama a [Accept()](../../../aspose.words/node/accept/) para todos los nodos hijos de este bloque de construcción, y luego llama a [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Nota: Un nodo de bloque de construcción y sus hijos no se visitan cuando ejecutas un Visitor sobre un [Document](../../../aspose.words/document/). Si deseas ejecutar un Visitor sobre un bloque de construcción, debes ejecutar el visitante sobre [GlossaryDocument](../../glossarydocument/) o llamar a [Accept()](./).

## Ver también

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
