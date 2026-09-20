---
title: "Метод Accept класса Aspose::Words::Fields::FieldStart"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Accept класса Aspose::Words::Fields::FieldStart. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
