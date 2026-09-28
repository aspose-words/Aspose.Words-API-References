---
title: "Aspose::Words::SpecialChar::Accept метод"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SpecialChar::Accept метод. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/specialchar/accept/
---
## SpecialChar::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::SpecialChar::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitSpecialChar()](../../documentvisitor/visitspecialchar/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SpecialChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
