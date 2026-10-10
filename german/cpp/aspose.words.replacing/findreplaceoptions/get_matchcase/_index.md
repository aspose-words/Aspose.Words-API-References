---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase-Methode"
linktitle: "get_MatchCase"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase-Methode. True gibt an, dass ein case-sensitiver Vergleich durchgeführt wird, false gibt an, dass ein case-insensitiver Vergleich durchgeführt wird in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True zeigt einen case‑sensitiven Vergleich an, false zeigt einen case‑insensitiven Vergleich an.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Beispiele



Zeigt, wie die Groß‑/Kleinschreibung bei einer Suchen‑und‑Ersetzen‑Operation umgeschaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das "MatchCase"‑Flag auf "true", um bei der Suche nach zu ersetzenden Zeichenketten die Groß‑/Kleinschreibung zu berücksichtigen.
// Setzen Sie das "MatchCase"‑Flag auf "false", um die Groß‑/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
