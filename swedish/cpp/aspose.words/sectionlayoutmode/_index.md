---
title: "Aspose::Words::SectionLayoutMode-enum"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::SectionLayoutMode-enum. Anger layoutläget för en sektion som möjliggör att definiera dokumentrutnätsbeteendet i C++."
type: docs
weight: 115000
url: /sv/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Anger layoutläget för ett avsnitt som möjliggör att definiera dokumentrutnätsbeteendet.

```cpp
enum class SectionLayoutMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Standard | 0 | Anger att inget dokumentrutnät ska tillämpas på innehållet i den motsvarande sektionen i dokumentet. |
| Rutnät | 1 | Anger att den motsvarande sektionen ska ha både extra radavstånd och teckenavstånd tillagt till varje rad och tecken i den för att upprätthålla ett specifikt antal rader per sida och tecken per rad. Tecken kommer inte automatiskt att justeras med rutnätslinjer vid skrivning. |
| LineGrid | 2 | Anger att den motsvarande sektionen ska ha extra radavstånd tillagt till varje rad i den för att upprätthålla det angivna antalet rader per sida. |
| SnapToChars | 3 | Anger att motsvarande avsnitt ska ha både extra radavstånd och teckenavstånd tillagt för varje rad och tecken i det för att upprätthålla ett specifikt antal rader per sida och tecken per rad. Tecken kommer automatiskt att justeras med rutnätslinjer vid skrivning. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
