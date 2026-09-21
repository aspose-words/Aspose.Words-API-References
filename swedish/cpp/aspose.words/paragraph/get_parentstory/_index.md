---
title: "Aspose::Words::Paragraph::get_ParentStory metod"
linktitle: "get_ParentStory"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::get_ParentStory metod. Hämtar den överordnade avsnittsnivå‑storyn som kan vara Body eller HeaderFooter i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words/paragraph/get_parentstory/
---
## Paragraph::get_ParentStory method


Hämtar föräldraavsnittsnivåns berättelse som kan vara [Body](../../body/) eller [HeaderFooter](../../headerfooter/).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::Paragraph::get_ParentStory()
```


## Exempel



Visar hur man skapar ett sidhuvud och en sidfot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett sidhuvud och lägg till ett stycke i det. Texten i det stycket
// kommer att visas högst upp på varje sida i detta avsnitt, ovanför huvudtexten.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Skapa en sidfot och lägg till ett stycke i den. Texten i det stycket
// kommer att visas längst ner på varje sida i detta avsnitt, under huvudtexten.
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

## Se även

* Class [Story](../../story/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
