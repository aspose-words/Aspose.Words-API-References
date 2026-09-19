---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart metodo"
linktitle: "VisitGlossaryDocumentStart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart metodo. Chiamato quando l'enumerazione di un documento glossario è iniziata in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


Chiamato quando inizia l'enumerazione di un documento di glossario.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| glossary | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | L'oggetto che viene visitato. |

### ReturnValue

Un valore [VisitorAction](../../visitoraction/) che specifica come continuare l'enumerazione.
## Note


Nota: Un nodo di documento glossario e i suoi figli non vengono visitati quando esegui un Visitor su un [Document](../../document/). Se vuoi eseguire un Visitor su un documento glossario, devi chiamare [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## Vedi anche

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
