---
title: "Aspose::Words::Story::AppendParagraph Methode"
linktitle: "AppendParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Story::AppendParagraph Methode. Eine Kurzmethode, die ein Paragraph-Objekt mit optionalem Text erstellt und es an das Ende dieses Objekts in C++ anhängt."
type: docs
weight: 2000
url: /de/cpp/aspose.words/story/appendparagraph/
---
## Story::AppendParagraph method


Eine Kurzmethode, die ein [Paragraph](../../paragraph/) Objekt mit optionalem Text erstellt und es an das Ende dieses Objekts anhängt.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::AppendParagraph(const System::String &text)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | const System::String\& | Der Text für den Absatz. Kann **null** oder eine leere Zeichenkette sein. |

### ReturnValue

Der neu erstellte und angehängte Absatz.

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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
