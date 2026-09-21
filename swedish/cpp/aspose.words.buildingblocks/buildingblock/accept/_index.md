---
title: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept‑metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept‑metod. Accepterar en besökare i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noderna. |

### ReturnValue

Sant om alla noder har besökts; falskt om [DocumentVisitor](../../../aspose.words/documentvisitor/) stoppade operationen innan alla noder besöktes.
## Anmärkningar


Enumererar denna nod och alla dess barn. Varje nod anropar en motsvarande metod på [DocumentVisitor](../../../aspose.words/documentvisitor/).

För mer information, se Visitor-designmönstret.

Anropar [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/), sedan anropar den [Accept()](../../../aspose.words/node/accept/) för alla underordnade noder i detta byggblock, och slutligen anropar den [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Obs: En byggblocknod och dess undernoder besöks inte när du kör en Visitor över ett [Document](../../../aspose.words/document/). Om du vill köra en Visitor över ett byggblock måste du köra besökaren över [GlossaryDocument](../../glossarydocument/) eller anropa [Accept()](./).

## Se även

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
