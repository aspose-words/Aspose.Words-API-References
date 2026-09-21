---
title: "Aspose::Words::Story::AppendParagraph metod"
linktitle: "AppendParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Story::AppendParagraph metod. En genvägsmetod som skapar ett Paragraph‑objekt med valfri text och lägger till det i slutet av detta objekt i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/story/appendparagraph/
---
## Story::AppendParagraph method


En genvägsmetod som skapar ett [Paragraph](../../paragraph/) objekt med valfri text och lägger till det i slutet av detta objekt.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::AppendParagraph(const System::String &text)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | const System::String\& | Texten för stycket. Kan vara **null** eller en tom sträng. |

### ReturnValue

Det nyss skapade och tillagda stycket.

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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
