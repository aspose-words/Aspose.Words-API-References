---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart метод"
linktitle: "VisitFieldStart"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart метод. Вызывается, когда поле начинается в документе в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Вызывается, когда в документе начинается поле.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | Объект, который посещается. |

### ReturnValue

Значение [VisitorAction](../../visitoraction/), которое указывает, как продолжить перечисление.
## Примечания


Поле в документе Word состоит из кода поля и значения поля.

Например, поле, отображающее номер страницы, может быть представлено следующим образом:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Разделитель полей отделяет код поля от значения поля в документе. Обратите внимание, что некоторые поля содержат только код поля и не имеют разделителя полей и значения поля.

[Fields](../../../aspose.words.fields/) can be nested.

## См. также

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
