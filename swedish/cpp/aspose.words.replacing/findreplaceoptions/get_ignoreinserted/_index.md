---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted metod"
linktitle: "get_IgnoreInserted"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted metod. Hämtar eller anger ett booleskt värde som indikerar om text inuti infogade revisioner ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Hämtar eller anger ett booleskt värde som indikerar om text inuti infogningsrevisioner ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Exempel



Visar hur man inkluderar eller ignorerar text i infogade revisioner under en sök‑och‑ersätt‑operation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Starta spårning av revisioner och infoga ett stycke. Det stycket kommer att vara en infogad revision.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "IgnoreInserted" till "true" för att få sök‑och‑ersätt
// operationen att ignorera stycken som är infogade revisioner.
// Ställ in flaggan "IgnoreInserted" till "false" för att få sök‑och‑ersätt
// operationen att också söka efter text i infogade revisioner.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
