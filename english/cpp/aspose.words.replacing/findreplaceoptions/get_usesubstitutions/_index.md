---
title: Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions method
linktitle: get_UseSubstitutions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions method. Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is false in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
```


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


Shows how to replace the text with substitutions. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "UseSubstitutions" property to "true" to get
// the find-and-replace operation to recognize substitution elements.
// Set the "UseSubstitutions" property to "false" to ignore substitution elements.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
