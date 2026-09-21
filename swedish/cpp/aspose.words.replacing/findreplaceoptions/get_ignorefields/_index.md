---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields metod"
linktitle: "get_IgnoreFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields‑metoden. Hämtar eller anger ett booleskt värde som indikerar om text inuti fält ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Hämtar eller anger ett booleskt värde som indikerar om text inuti fält ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Anmärkningar


Det här alternativet påverkar hela fältet (alla noder mellan [FieldStart](../../../aspose.words/nodetype/) och [FieldEnd](../../../aspose.words/nodetype/)).

För att bara ignorera fältkoder, använd det motsvarande alternativet [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Exempel



Visar hur man ignorerar text i fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "IgnoreFields" till "true" för att få sök‑och‑ersätt
// operationen att ignorera text i fält.
// Ställ in flaggan "IgnoreFields" till "false" för att få sök‑och‑ersätt
// operationen att även söka efter text i fält.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
