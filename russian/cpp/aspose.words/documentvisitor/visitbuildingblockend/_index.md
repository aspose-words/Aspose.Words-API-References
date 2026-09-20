---
title: "Метод Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd"
linktitle: "VisitBuildingBlockEnd"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd. Вызывается, когда перечисление строительного блока завершилось в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor::VisitBuildingBlockEnd method


Вызывается, когда перечисление строительного блока завершилось.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
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
