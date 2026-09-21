---
title: "Aspose::Words::OutlineLevel enum"
linktitle: "OutlineLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::OutlineLevel enum. Anger outline-nivån för ett stycke i dokumentet i C++."
type: docs
weight: 105000
url: /sv/cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


Anger dispositionsnivån för ett stycke i dokumentet.

```cpp
enum class OutlineLevel
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Level1 | 0 | Stycket är på outline-nivå 1 (högsta nivån). |
| Level2 | 1 | Stycket är på outline-nivå 2. |
| Level3 | 2 | Stycket är på outline-nivå 3. |
| Level4 | 3 | Stycket är på outline-nivå 4. |
| Level5 | 4 | Stycket är på outline-nivå 5. |
| Level6 | 5 | Stycket är på outline-nivå 6. |
| Level7 | 6 | Stycket är på outline-nivå 7. |
| Level8 | 7 | Stycket är på outline-nivå 8. |
| Level9 | 8 | Stycket är på outline-nivå 9. |
| BodyText | 9 | Stycket är på nivån för huvudtexten. |


## Exempel



Visar hur man konfigurerar stycke-outline-nivåer för att skapa hopfällbar text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Varje stycke har en OutlineLevel, som kan vara vilket tal som helst från 1 till 9, eller standardvärdet "BodyText".
// Att sätta egenskapen till ett av de numrerade värdena kommer att visa en pil till vänster
// vid början av stycket.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Nivå 1 är den högsta nivån. Om det finns ett stycke med en lägre nivå under ett stycke med en högre nivå,
// Att fälla ihop det högre nivåstycket kommer att fälla ihop det lägre nivåstycket.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Två stycken på samma nivå kommer inte att fälla ihop varandra,
// och pilarna fäller inte ihop de stycken de pekar på.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// Standardvärdet "BodyText" är det lägsta, vilket ett stycke på vilken nivå som helst kan fälla ihop.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
