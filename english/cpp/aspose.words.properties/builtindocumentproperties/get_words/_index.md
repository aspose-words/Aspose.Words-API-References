---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_Words method
linktitle: get_Words
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_Words method. Represents an estimate of the number of words in the document in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_words/
---
## BuiltInDocumentProperties::get_Words method


Represents an estimate of the number of words in the document.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Words()
```

## Remarks


Aspose.Words updates this property when you call [UpdateWordCount](../../../aspose.words/document/updatewordcount/).
## Examples


Shows how to update all list labels in a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words does not track document metrics like these in real time.
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Characters(), 0);
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Words(), 0);
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Paragraphs(), 1);
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Lines(), 1);

// To get accurate values for three of these properties, we will need to update them manually.
doc->UpdateWordCount();

ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Characters(), 196);
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Words(), 36);
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Paragraphs(), 2);

// For the line count, we will need to call a specific overload of the updating method.
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Lines(), 1);

doc->UpdateWordCount(true);

ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Lines(), 4);
```
## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
