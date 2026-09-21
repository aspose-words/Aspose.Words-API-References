---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted metod"
linktitle: "get_IgnoreDeleted"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted metod. Hämtar eller anger ett booleskt värde som indikerar om text inuti raderingsrevisioner ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Hämtar eller anger ett booleskt värde som indikerar om text inuti raderingsrevisioner ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Exempel



Visar hur man inkluderar eller ignorerar text inuti raderingsrevisioner under en sök‑och‑ersätt‑operation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Starta spårning av revisioner och ta bort det andra stycket, vilket kommer att skapa en raderingsrevision.
// Det stycket kommer att finnas kvar i dokumentet tills vi accepterar raderingsrevisionen.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Vi kan använda ett "FindReplaceOptions"‑objekt för att ändra sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "IgnoreDeleted" till "true" för att få sök‑och‑ersätt
// operationen att ignorera stycken som är raderingsrevisioner.
// Ställ in flaggan "IgnoreDeleted" till "false" för att få sök‑och‑ersätt
// operationen att också söka efter text inuti raderingsrevisioner.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
