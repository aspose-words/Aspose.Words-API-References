---
title: "Aspose::Words::PageSetup::get_CharactersPerLine-metod"
linktitle: "get_CharactersPerLine"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_CharactersPerLine-metod. Hämtar eller anger antalet tecken per rad i dokumentrutnätet i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Hämtar eller anger antalet tecken per rad i dokumentrutnätet.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Anmärkningar


Minimivärdet för egenskapen är 1. Maximivärdet beror på sidbredd och teckenstorlek för Normal-stilen. Minsta teckenavstånd är 90 procent av teckenstorleken. Till exempel är maximalt antal tecken per rad på ett Letter-blad med en-tumsmarginaler 43.

Som standard har egenskapen ett värde där teckenavståndet är lika med teckenstorleken för Normal-stilen.

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

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
