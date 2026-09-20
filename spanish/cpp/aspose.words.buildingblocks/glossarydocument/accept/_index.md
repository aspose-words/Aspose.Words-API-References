---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept método"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept método. Acepta un visitante en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará los nodos. |

### ReturnValue

Verdadero si se visitaron todos los nodos; falso si [DocumentVisitor](../../../aspose.words/documentvisitor/) detuvo la operación antes de visitar todos los nodos.
## Observaciones


Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en [DocumentVisitor](../../../aspose.words/documentvisitor/).

Para más información, consulte el patrón de diseño Visitor.

Llama a [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/), luego llama a [Accept()](../../../aspose.words/node/accept/) para todos los nodos hijos de este nodo y después llama a [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) al final.

Nota: Un nodo de documento de glosario y sus hijos no se visitan cuando ejecutas un Visitor sobre un [Document](../../../aspose.words/document/). Si deseas ejecutar un Visitor sobre un documento de glosario, necesitas llamar a [Accept()](./).

## Ver también

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
