---
title: "Aspose::Words::Notes::EndnotePosition enum"
linktitle: "EndnotePosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::EndnotePosition enum. Definierar slutnotens position i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.notes/endnoteposition/
---
## EndnotePosition enum


Definierar slutnotens position.

```cpp
enum class EndnotePosition
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| EndOfSection | 0 | Slutnoter skrivs ut i slutet av avsnittet. |
| EndOfDocument | 3 | Slutnoter skrivs ut i slutet av dokumentet. |


## Exempel



Visar hur man väljer en annan plats där dokumentet samlar och visar sina slutnoter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// En slutnot är ett sätt att bifoga en referens eller en sidokommentar till text
// som inte stör huvudtextens flöde.
// Att infoga en slutnot lägger till en liten upphöjd referenssymbol
// i huvudtexten där vi infogar slutnoten.
// Varje slutnot skapar också ett post i slutet av dokumentet, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Vi kan använda egenskapen "Position" för att bestämma var dokumentet placerar alla sina slutnoter.
// Om vi sätter värdet på egenskapen "Position" till "EndnotePosition.EndOfDocument",
// kommer varje fotnot att visas i en samling i slutet av dokumentet. Detta är standardvärdet.
// Om vi sätter värdet på egenskapen "Position" till "EndnotePosition.EndOfSection",
// kommer varje fotnot att visas i en samling i slutet av avsnittet vars text innehåller slutnotens referensmärke.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## Se även

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
