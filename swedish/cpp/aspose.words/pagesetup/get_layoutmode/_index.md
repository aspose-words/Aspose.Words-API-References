---
title: "Aspose::Words::PageSetup::get_LayoutMode metod"
linktitle: "get_LayoutMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_LayoutMode metod. Hämtar eller sätter layoutläget för detta avsnitt i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words/pagesetup/get_layoutmode/
---
## PageSetup::get_LayoutMode method


Hämtar eller anger layoutläget för detta avsnitt.

```cpp
Aspose::Words::SectionLayoutMode Aspose::Words::PageSetup::get_LayoutMode()
```


## Exempel



Visar hur man anger ett värde för antalet tecken som varje rad kan ha.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aktivera pitchning och använd sedan den för att ställa in antalet tecken per rad i detta avsnitt.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Antalet tecken beror också på teckensnittets storlek.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```


Visar hur man anger en gräns för antalet rader som varje sida kan ha.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aktivera pitchning och använd sedan den för att ställa in antalet rader per sida i detta avsnitt.
// En tillräckligt stor teckensnittsstorlek kommer att skjuta ner vissa rader till nästa sida för att undvika överlappande tecken.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Se även

* Enum [SectionLayoutMode](../../sectionlayoutmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
