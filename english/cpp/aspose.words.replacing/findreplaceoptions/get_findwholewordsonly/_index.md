---
title: Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly method
linktitle: get_FindWholeWordsOnly
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly method. True indicates the oldValue must be a standalone word in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True indicates the oldValue must be a standalone word.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Examples



Shows how to toggle standalone word-only find-and-replace operations. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
