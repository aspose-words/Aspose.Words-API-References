---
title: "Aspose::Words::Paragraph::get_ParentStory Methode"
linktitle: "get_ParentStory"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::get_ParentStory Methode. Ruft die übergeordnete Story auf Abschnittsebene ab, die Body oder HeaderFooter sein kann, in C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words/paragraph/get_parentstory/
---
## Paragraph::get_ParentStory method


Ruft die übergeordnete Story auf Abschnittsebene ab, die [Body](../../body/) oder [HeaderFooter](../../headerfooter/) sein kann.

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::Paragraph::get_ParentStory()
```


## Beispiele



Zeigt, wie man eine Kopfzeile und eine Fußzeile erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle eine Kopfzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts angezeigt, über dem Haupttext.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Erstelle eine Fußzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts angezeigt, unter dem Haupttext.
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

## Siehe auch

* Class [Story](../../story/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
