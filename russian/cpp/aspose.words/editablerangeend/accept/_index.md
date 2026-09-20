---
title: "Метод Aspose::Words::EditableRangeEnd::Accept"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::EditableRangeEnd::Accept. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
