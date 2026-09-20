---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart método"
linktitle: "VisitGlossaryDocumentStart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart método. Llamado cuando la enumeración de un documento de glosario ha comenzado en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


Se llama cuando la enumeración de un documento de glosario ha comenzado.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
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
