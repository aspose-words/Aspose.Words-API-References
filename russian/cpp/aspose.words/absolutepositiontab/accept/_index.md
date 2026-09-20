---
title: "Aspose::Words::AbsolutePositionTab::Accept метод"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AbsolutePositionTab::Accept метод. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
