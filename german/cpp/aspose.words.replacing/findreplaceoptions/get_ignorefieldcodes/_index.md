---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes Methode"
linktitle: "get_IgnoreFieldCodes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. Der Standardwert ist false in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Hinweise


Diese Option wirkt nur auf Feldcodes (sie ignoriert keine Knoten zwischen [FieldSeparator](../../../aspose.words/nodetype/) und [FieldEnd](../../../aspose.words/nodetype/)).

Um das gesamte Feld zu ignorieren, verwenden Sie bitte die entsprechende Option [IgnoreFields](../get_ignorefields/).

## Beispiele



Zeigt, wie man Text innerhalb von Feldcodes ignoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Ersetzt 'T' im Dokument, wobei Text innerhalb von Feldcodes ignoriert wird oder nicht.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
