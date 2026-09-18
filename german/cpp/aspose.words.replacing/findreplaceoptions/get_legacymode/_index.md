---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode-Methode"
linktitle: "get_LegacyMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode-Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, dass der alte Find/Replace-Algorithmus in C++ verwendet wird."
type: docs
weight: 13000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Liest oder setzt einen booleschen Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
```


## Beispiele



Zeigt, wie man Substitutionen innerhalb von Ersetzungsmustern erkennt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Die Verwendung des Legacy‑Modus unterstützt viele erweiterte Funktionen nicht, daher müssen wir ihn auf 'false' setzen.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
