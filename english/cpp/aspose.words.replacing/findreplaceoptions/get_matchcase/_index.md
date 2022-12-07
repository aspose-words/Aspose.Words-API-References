---
title: get_MatchCase
second_title: Aspose.Words for C++ API Reference
description: True indicates case-sensitive comparison, false indicates case-insensitive comparison.
type: docs
weight: 170
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? String(u"Jade bought a ruby necklace.") : String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words](../../../)
