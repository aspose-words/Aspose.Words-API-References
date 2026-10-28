---
title: Aspose::Words::Replacing::FindReplaceOptions::set_LegacyMode method
linktitle: set_LegacyMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::set_LegacyMode method. Sets a boolean value indicating that old find/replace algorithm is used in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words.replacing/findreplaceoptions/set_legacymode/
---
## FindReplaceOptions::set_LegacyMode method


Sets a boolean value indicating that old find/replace algorithm is used.

```cpp
void Aspose::Words::Replacing::FindReplaceOptions::set_LegacyMode(bool value)
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
