---
title: "Aspose::Words::Paragraph::get_IsFormatRevision method"
linktitle: "get_IsFormatRevision"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Paragraph::get_IsFormatRevision. Возвращает true, если форматирование объекта было изменено в Microsoft Word при включённом отслеживании изменений в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Возвращает true, если форматирование объекта было изменено в Microsoft Word при включённом отслеживании изменений.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Примеры



Показывает, как проверить, является ли абзац ревизией форматирования.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Этот абзац является ревизией "Format", которая происходит, когда мы изменяем форматирование существующего текста.
// во время отслеживания правок в Microsoft Word через «Review» -> «Track changes».
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
