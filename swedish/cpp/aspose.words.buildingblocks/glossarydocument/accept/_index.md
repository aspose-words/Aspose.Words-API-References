---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept metod. Accepterar en besökare i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noderna. |

### ReturnValue

Sant om alla noder har besökts; falskt om [DocumentVisitor](../../../aspose.words/documentvisitor/) stoppade operationen innan alla noder besöktes.
## Anmärkningar


Enumererar denna nod och alla dess barn. Varje nod anropar en motsvarande metod på [DocumentVisitor](../../../aspose.words/documentvisitor/).

För mer information, se Visitor-designmönstret.

Anropar [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/), sedan anropar den [Accept()](../../../aspose.words/node/accept/) för alla undernoder till denna nod och slutligen anropar [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) i slutet.

Obs: En glossariedokumentnod och dess undernoder besöks inte när du kör en Visitor över ett [Document](../../../aspose.words/document/). Om du vill köra en Visitor över ett glossariedokument måste du anropa [Accept()](./).

## Se även

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
