---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode metod"
linktitle: "get_LegacyMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode metod. Hämtar eller anger ett booleskt värde som indikerar att den gamla sök/ersätt-algoritmen används i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Hämtar eller anger ett booleskt värde som indikerar att den gamla sök/ersätt-algoritmen används.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
```


## Exempel



Visar hur man känner igen och använder substitutioner inom ersättningsmönster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Att använda legacy‑läge stöder inte många avancerade funktioner, så vi måste sätta det till 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
