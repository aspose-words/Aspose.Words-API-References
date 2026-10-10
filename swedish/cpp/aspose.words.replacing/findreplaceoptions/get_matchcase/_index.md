---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase metod"
linktitle: "get_MatchCase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase metod. True indikerar skiftlägeskänslig jämförelse, false indikerar skiftlägesokänslig jämförelse i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True indikerar skiftlägeskänslig jämförelse, false indikerar skiftlägesokänslig jämförelse.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Exempel



Visar hur man växlar skiftlägeskänslighet vid en sök‑och‑ersätt‑operation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "MatchCase" till "true" för att tillämpa skiftlägeskänslighet när du söker efter strängar att ersätta.
// Ställ in flaggan "MatchCase" till "false" för att ignorera teckenkänslighet när du söker efter text att ersätta.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
