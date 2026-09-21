---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly metod"
linktitle: "get_FindWholeWordsOnly"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly metod. True indikerar att oldValue måste vara ett fristående ord i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True indikerar att oldValue måste vara ett fristående ord.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Exempel



Visar hur man växlar fristående ord‑endast sök‑och‑ersätt‑operationer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "FindWholeWordsOnly" till "true" för att ersätta den hittade texten om den inte är en del av ett annat ord.
// Ställ in flaggan "FindWholeWordsOnly" till "false" för att ersätta all text oavsett dess omgivning.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
