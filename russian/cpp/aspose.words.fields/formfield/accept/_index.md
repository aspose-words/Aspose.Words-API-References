---
title: "Метод Aspose::Words::Fields::FormField::Accept"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FormField::Accept. Принимает посетителя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/formfield/accept/
---
## FormField::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::Fields::FormField::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Примечания


Вызовы [VisitFormField()](../../../aspose.words/documentvisitor/visitformfield/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
