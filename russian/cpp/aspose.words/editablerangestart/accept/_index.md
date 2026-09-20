---
title: "Метод Aspose::Words::EditableRangeStart::Accept"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::EditableRangeStart::Accept. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/editablerangestart/accept/
---
## EditableRangeStart::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::EditableRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitEditableRangeStart()](../../documentvisitor/visiteditablerangestart/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
