---
title: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator metod"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator metod. Sant om detta styckebrott är en stilseparator. En stilseparator tillåter ett stycke att bestå av delar som har olika styckeformat i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


Sant om detta styckebrott är en [Style](../../style/) Separator. En stilseparator tillåter ett stycke att bestå av delar som har olika styckeformat.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Exempel



Visar hur man skriver text på samma rad som en TOC‑rubrik utan att den visas i TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Infoga ett stycke med en stil som TOC:n kommer att plocka upp som ett objekt.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Båda dessa strängar är i samma stycke och kommer därför att visas i samma TOC‑objekt.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Om vi infogar en stilseparator kan vi skriva mer text i samma stycke
// och använda en annan stil utan att den visas i TOC.
// Om vi använder en rubriktypstil efter separatorn kan vi skapa flera TOC‑objekt från en dokumenttextrad.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## Se även

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
