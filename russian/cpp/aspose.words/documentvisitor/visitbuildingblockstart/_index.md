---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart метод"
linktitle: "VisitBuildingBlockStart"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart метод. Вызывается, когда начинается перечисление строительного блока в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor::VisitBuildingBlockStart method


Вызывается, когда перечисление строительного блока началось.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockStart(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| блок | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | Объект, который посещается. |

### ReturnValue

Значение [VisitorAction](../../visitoraction/), которое указывает, как продолжить перечисление.
## Примечания


Примечание: Узел строительного блока и его дочерние элементы не посещаются, когда вы выполняете Visitor над [Document](../../document/). Если вы хотите выполнить Visitor над строительным блоком, вам необходимо выполнить Visitor над [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) или вызвать [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## См. также

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
