---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions method"
linktitle: "get_UseSubstitutions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions method. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Liest oder setzt einen booleschen Wert, der angibt, ob Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
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


Zeigt, wie man den Text mit Substitutionen ersetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie die Eigenschaft "UseSubstitutions" auf "true", um zu erhalten
// den Suchen‑und‑Ersetzen‑Vorgang, um Substitutionselemente zu erkennen.
// Setzen Sie die Eigenschaft "UseSubstitutions" auf "false", um Substitutionselemente zu ignorieren.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
