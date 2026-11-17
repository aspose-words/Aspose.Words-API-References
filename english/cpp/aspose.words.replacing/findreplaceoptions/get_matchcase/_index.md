---
title: Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase method
linktitle: get_MatchCase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase method. True indicates case-sensitive comparison, false indicates case-insensitive comparison in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True indicates case-sensitive comparison, false indicates case-insensitive comparison.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Examples



Shows how to toggle case sensitivity when performing a find-and-replace operation. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
