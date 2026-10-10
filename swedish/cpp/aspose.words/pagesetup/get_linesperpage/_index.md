---
title: "Aspose::Words::PageSetup::get_LinesPerPage metod"
linktitle: "get_LinesPerPage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_LinesPerPage metod. Hämtar eller anger antalet rader per sida i dokumentrutnätet i C++."
type: docs
weight: 26000
url: /sv/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Hämtar eller anger antalet rader per sida i dokumentrutnätet.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Anmärkningar


Minimivärdet för egenskapen är 1. Maximivärdet beror på sidans höjd och teckensnittsstorleken för Normal‑stilen. Minsta radavstånd är 136 procent av teckensnittsstorleken. Till exempel är maximalt antal rader per sida på ett Letter‑blad med en‑tums marginaler 39.

Som standard har egenskapen ett värde där radavståndet är 1,5 gånger större än teckensnittsstorleken för Normal‑stilen.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
