---
title: "Метод Aspose::Words::BuildingBlocks::BuildingBlock::Accept"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BuildingBlocks::BuildingBlock::Accept. Принимает посетителя в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет обходить узлы. |

### ReturnValue

True, если все узлы были посещены; false, если [DocumentVisitor](../../../aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.
## Примечания


Перебирает этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод у [DocumentVisitor](../../../aspose.words/documentvisitor/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

Вызывает [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/), затем вызывает [Accept()](../../../aspose.words/node/accept/) для всех дочерних узлов этого строительного блока, затем вызывает [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Примечание: Узел строительного блока и его дочерние элементы не посещаются, когда вы выполняете Visitor над [Document](../../../aspose.words/document/). Если вы хотите выполнить Visitor над строительным блоком, вам необходимо выполнить посетитель над [GlossaryDocument](../../glossarydocument/) или вызвать [Accept()](./).

## См. также

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
