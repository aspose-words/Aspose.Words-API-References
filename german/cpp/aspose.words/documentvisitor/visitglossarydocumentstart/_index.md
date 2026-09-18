---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart Methode"
linktitle: "VisitGlossaryDocumentStart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart Methode. Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments in C++ begonnen hat."
type: docs
weight: 28000
url: /de/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments begonnen hat.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Glossar | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | Das Objekt, das besucht wird. |

### ReturnValue

Ein [VisitorAction](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.
## Hinweise


Hinweis: Ein Glossar-Dokumentknoten und seine Unterelemente werden nicht besucht, wenn Sie einen Visitor über ein [Dokument](../../document/) ausführen. Wenn Sie einen Visitor über ein Glossar-Dokument ausführen möchten, müssen Sie [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/) aufrufen.

## Siehe auch

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
