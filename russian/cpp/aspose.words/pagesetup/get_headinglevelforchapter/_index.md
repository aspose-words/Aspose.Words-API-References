---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter метод"
linktitle: "get_HeadingLevelForChapter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter метод. Получает или задает стиль уровня заголовка, применяемый к названиям глав в документе в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Получает или задает стиль уровня заголовка, применяемый к названиям глав в документе.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Примечания


Может быть числом от 0 до 9. 0 означает отсутствие номера главы, если применяется к номеру страницы.

Прежде чем вы сможете создавать номера страниц, включающие номера глав, заголовки документа должны иметь примененный нумерованный формат структуры.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
