---
title: "Метод Aspose::Words::DocumentVisitor::VisitFieldSeparator"
linktitle: "VisitFieldSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentVisitor::VisitFieldSeparator. Вызывается, когда в документе в C++ встречается разделитель полей."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Вызывается, когда в документе встречается разделитель полей.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | Объект, который посещается. |

### ReturnValue

Значение [VisitorAction](../../visitoraction/), которое указывает, как продолжить перечисление.
## Примечания


Разделитель полей отделяет код поля от значения поля в документе. Обратите внимание, что некоторые поля содержат только код поля и не имеют разделителя полей и значения поля.

Для получения дополнительной информации см. [VisitFieldStart()](../visitfieldstart/)

## См. также

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
