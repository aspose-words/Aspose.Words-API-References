---
title: Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields method
linktitle: get_IgnoreFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields method. Gets or sets a boolean value indicating either to ignore text inside fields. The default value is false in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Gets or sets a boolean value indicating either to ignore text inside fields. The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Remarks


This option affects whole field (all nodes between [FieldStart](../../../aspose.words/nodetype/) and [FieldEnd](../../../aspose.words/nodetype/)).

To ignore only field codes, please use corresponding option [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Examples



Shows how to ignore text inside fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "IgnoreFields" flag to "true" to get the find-and-replace
// operation to ignore text inside fields.
// Set the "IgnoreFields" flag to "false" to get the find-and-replace
// operation to also search for text inside fields.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
