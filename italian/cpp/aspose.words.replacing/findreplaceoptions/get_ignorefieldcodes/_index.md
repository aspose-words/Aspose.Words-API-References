---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method"
linktitle: "get_IgnoreFieldCodes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method. Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno dei codici di campo. Il valore predefinito è false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno dei codici di campo. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Note


Questa opzione influisce solo sui codici di campo (non ignora i nodi tra [FieldSeparator](../../../aspose.words/nodetype/) e [FieldEnd](../../../aspose.words/nodetype/)).

Per ignorare l'intero campo, si prega di utilizzare l'opzione corrispondente [IgnoreFields](../get_ignorefields/).

## Esempi



Mostra come ignorare il testo all'interno dei codici di campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Sostituisci 'T' nel documento ignorando il testo all'interno del codice campo o meno.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
