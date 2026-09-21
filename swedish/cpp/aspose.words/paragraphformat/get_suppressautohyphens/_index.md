---
title: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens metod"
linktitle: "get_SuppressAutoHyphens"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens metod. Anger om det aktuella stycket ska undantas från eventuell avstavning som tillämpas i dokumentinställningarna i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Anger om det aktuella stycket ska undantas från eventuell avstavning som tillämpas i dokumentinställningarna.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Exempel



Visar hur man undertrycker avstavning för ett stycke.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Öppna ett dokument som innehåller text med en lokalkod som matchar vår ordbok.
// När vi sparar detta dokument i ett fast sidformat kommer dess text att ha avstavning.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Vi kan sätta egenskapen "SuppressAutoHyphens" till "true" för att inaktivera avstavning
// för ett specifikt stycke samtidigt som den hålls aktiverad för resten av dokumentet.
// Standardvärdet för denna egenskap är "false",
// vilket betyder att varje stycke som standard använder avstavning om någon finns tillgänglig.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
