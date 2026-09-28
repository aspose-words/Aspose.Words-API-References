---
title: "Aspose::Words::DocumentBuilder::MoveToSection method"
linktitle: "MoveToSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::MoveToSection method. Перемещает курсор в начало тела в указанном разделе в C++."
type: docs
weight: 60000
url: /ru/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Перемещает курсор в начало тела в указанном разделе.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionIndex | int32_t | Индекс раздела, к которому нужно переместиться. |
## Примечания


Когда *sectionIndex* больше или равен 0, он указывает индекс от начала документа, где 0 — первый раздел. Когда *sectionIndex* меньше 0, он указывает индекс от конца документа, где -1 — последний раздел.

Курсор перемещается к первому абзацу в [Body](../../body/) указанного раздела.

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
