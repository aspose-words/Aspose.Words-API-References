---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ChapterPageSeparator enum. Определяет символ-разделитель, который появляется между номером главы и страницей в C++."
type: docs
weight: 84000
url: /ru/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Определяет символ-разделитель, который появляется между номером главы и номером страницы.

```cpp
enum class ChapterPageSeparator
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Дефис | 0 | Двоеточие. |
| Точка | 1 | Точка. |
| Двоеточие | 2 | Двоеточие. |
| EmDash | 3 | Выделенное тире. |
| EnDash | 4 | Стандартное тире. |


## Примеры



Показывает, как работать с главами страниц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
