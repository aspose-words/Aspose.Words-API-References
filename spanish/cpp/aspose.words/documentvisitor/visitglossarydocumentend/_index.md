---
title: "Método Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd"
linktitle: "VisitGlossaryDocumentEnd"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd. Llamado cuando la enumeración de un documento de glosario ha finalizado en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


Se llama cuando la enumeración de un documento de glosario ha finalizado.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| glosario | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | El objeto que está siendo visitado. |

### ReturnValue

Un valor [VisitorAction](../../visitoraction/) que especifica cómo continuar la enumeración.
## Observaciones


Nota: Un nodo de documento de glosario y sus hijos no son visitados cuando ejecutas un Visitor sobre un [Document](../../document/). Si deseas ejecutar un Visitor sobre un documento de glosario, debes llamar a [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## Ver también

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
