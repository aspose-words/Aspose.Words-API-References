---
title: Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method
linktitle: get_IgnoreFieldCodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method. Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is false in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Remarks


This option affects only field codes (it does not ignore nodes between [FieldSeparator](../../../aspose.words/nodetype/) and [FieldEnd](../../../aspose.words/nodetype/)).

To ignore whole field, please use corresponding option [IgnoreFields](../get_ignorefields/).

## Examples



Shows how to ignore text inside field codes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Replace 'T' in document ignoring text inside field code or not.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
