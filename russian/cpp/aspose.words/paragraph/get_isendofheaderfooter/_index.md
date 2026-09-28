---
title: "Aspose::Words::Paragraph::get_IsEndOfHeaderFooter метод"
linktitle: "get_IsEndOfHeaderFooter"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Paragraph::get_IsEndOfHeaderFooter. Истина, если этот абзац является последним абзацем в HeaderFooter (основная текстовая история) Section; иначе ложь в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/paragraph/get_isendofheaderfooter/
---
## Paragraph::get_IsEndOfHeaderFooter method


Истина, если этот абзац является последним абзацем в [HeaderFooter](../../headerfooter/) (основная текстовая история) [Section](../../section/); иначе ложь.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfHeaderFooter()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
