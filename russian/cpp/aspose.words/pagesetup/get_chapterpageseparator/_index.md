---
title: "Метод Aspose::Words::PageSetup::get_ChapterPageSeparator"
linktitle: "get_ChapterPageSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_ChapterPageSeparator. Получает или задает символ-разделитель, который появляется между номером главы и номером страницы в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Получает или задает символ-разделитель, который появляется между номером главы и номером страницы.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Примечания


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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
