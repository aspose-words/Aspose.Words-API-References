---
title: Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode method
linktitle: get_LegacyMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode method. Gets or sets a boolean value indicating that old find/replace algorithm is used in C++.'
type: docs
weight: 20671
url: /cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Gets or sets a boolean value indicating that old find/replace algorithm is used.

```cpp
_Bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
```

## Remarks

 Use this flag if you need exactly the same behavior as before advanced find/replace feature was introduced. Note that old algorithm does not support advanced features such as replace with breaks, apply formatting and so on. 
## Examples


Shows how to recognize and use substitutions within replacement patterns.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Using legacy mode does not support many advanced features, so we need to set it to 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```
## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
