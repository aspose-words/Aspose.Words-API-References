---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore method"
linktitle: "get_PageBreakBefore"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore method. Sant om en sidbrytning tvingas före stycket i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


Sant om en sidbrytning tvingas före stycket.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Exempel



Visar hur man skapar stycken med sidbrytningar i början.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in denna flagga till "true" för att tillämpa en sidbrytning i början av varje stycke
// som dokumentbyggaren kommer att skapa under denna ParagraphFormat‑konfiguration.
// Det första stycket kommer inte att få en sidbrytning.
// Lämna denna flagga som "false" för att börja varje nytt stycke på samma sida
// som det föregående, förutsatt att det finns tillräckligt med utrymme.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
