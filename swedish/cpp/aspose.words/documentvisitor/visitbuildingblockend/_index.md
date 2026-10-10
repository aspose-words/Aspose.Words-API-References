---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd metod"
linktitle: "VisitBuildingBlockEnd"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd metod. Anropas när uppräkning av ett byggblock har avslutats i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor::VisitBuildingBlockEnd method


Kallas när uppräkning av ett byggblock har avslutats.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| block | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | Objektet som besöks. |

### ReturnValue

Ett [VisitorAction](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.
## Anmärkningar


Obs: En byggblocknod och dess underordnade besöks inte när du kör en Visitor över ett [Document](../../document/). Om du vill köra en Visitor över ett byggblock måste du köra besökaren över [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) eller anropa [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## Se även

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
