---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "FootnotePosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnotePosition enum. Definierar fotnotens position i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


Definierar fotnotens position.

```cpp
enum class FootnotePosition
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| BottomOfPage | 1 | Fotnoter visas längst ner på varje sida. |
| BeneathText | 2 | Fotnoter visas under texten på varje sida. |


## Exempel



Visar hur man väljer en annan plats där dokumentet samlar och visar sina fotnoter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// En fotnot är ett sätt att bifoga en referens eller en sidokommentar till text
// som inte stör huvudtextens flöde.
// Att infoga en fotnot lägger till en liten upphöjd referenssymbol
// i huvudtexten där vi infogar fotnoten.
// Varje fotnot skapar också en post längst ner på sidan, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// Vi kan använda egenskapen "Position" för att bestämma var dokumentet placerar alla sina fotnoter.
// Om vi sätter värdet på egenskapen "Position" till "FootnotePosition.BottomOfPage",
// varje fotnot kommer att visas längst ner på sidan som innehåller dess referensmarkör. Detta är standardvärdet.
// Om vi sätter värdet på egenskapen "Position" till "FootnotePosition.BeneathText",
// varje fotnot kommer att visas i slutet av sidans text som innehåller dess referensmarkör.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## Se även

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
