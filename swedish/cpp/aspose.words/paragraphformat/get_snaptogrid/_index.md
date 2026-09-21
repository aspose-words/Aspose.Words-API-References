---
title: "Aspose::Words::ParagraphFormat::get_SnapToGrid metod"
linktitle: "get_SnapToGrid"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_SnapToGrid‑metod. Anger om det aktuella stycket ska använda dokumentets rutnätslinjer per sidinställning när innehållet i stycket läggs ut i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Anger om det aktuella stycket ska använda dokumentets rutnätslinjer per sida-inställningar vid layout av innehållet i stycket.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


## Exempel



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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
