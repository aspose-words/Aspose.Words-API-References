---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd metod"
linktitle: "VisitGlossaryDocumentEnd"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd metod. Anropas när uppräkning av ett glossariedokument har avslutats i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


Kallas när uppräkning av ett glossaridokument har avslutats.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| glossarium | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | Objektet som besöks. |

### ReturnValue

Ett [VisitorAction](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.
## Anmärkningar


Obs: En glossariedokumentnod och dess barn besöks inte när du kör en Visitor över ett [Document](../../document/). Om du vill köra en Visitor över ett glossariedokument måste du anropa [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## Se även

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
