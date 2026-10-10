---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel metod"
linktitle: "get_OutlineLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel method. Anger dispositionens nivå för stycket i dokumentet i C++."
type: docs
weight: 26000
url: /sv/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Anger konturnivån för stycket i dokumentet.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


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

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
