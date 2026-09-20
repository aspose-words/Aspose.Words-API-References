---
title: "Aspose::Words::Paragraph::get_ParentSection метод"
linktitle: "get_ParentSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::get_ParentSection метод. Получает родительский Section абзаца в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words/paragraph/get_parentsection/
---
## Paragraph::get_ParentSection method


Получает родительский [Section](../../section/) абзаца.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Paragraph::get_ParentSection()
```


## Примеры



Показывает, как создать заголовок и нижний колонтитул.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте заголовок и добавьте к нему абзац. Текст в этом абзаце
// будет отображаться в верхней части каждой страницы этого раздела, над основным текстом.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Создайте нижний колонтитул и добавьте к нему абзац. Текст в этом абзаце
// будет отображаться в нижней части каждой страницы этого раздела, под основным текстом.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## См. также

* Class [Section](../../section/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
