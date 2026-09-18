---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd Methode"
linktitle: "VisitBuildingBlockEnd"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd Methode. Wird aufgerufen, wenn die Enumeration eines Bausteins in C++ beendet ist."
type: docs
weight: 9000
url: /de/cpp/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor::VisitBuildingBlockEnd method


Wird aufgerufen, wenn die Aufzählung eines Bausteins beendet ist.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Block | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | Das Objekt, das besucht wird. |

### ReturnValue

Ein [VisitorAction](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.
## Hinweise


Hinweis: Ein Bausteinknoten und seine Kinder werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../document/) ausführen. Wenn Sie einen Visitor über einen Baustein ausführen möchten, müssen Sie den Visitor über ein [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) ausführen oder [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/) aufrufen.

## Siehe auch

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
