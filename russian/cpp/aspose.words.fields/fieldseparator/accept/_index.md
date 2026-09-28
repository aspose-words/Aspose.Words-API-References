---
title: "Aspose::Words::Fields::FieldSeparator::Accept метод"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldSeparator::Accept метод. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldseparator/accept/
---
## FieldSeparator::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::Fields::FieldSeparator::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitFieldSeparator()](../../../aspose.words/documentvisitor/visitfieldseparator/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldSeparator](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
