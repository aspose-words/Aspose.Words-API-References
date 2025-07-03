---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines method
linktitle: get_Lines
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines method. Represents an estimate of the number of lines in the document in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_lines/
---
## BuiltInDocumentProperties::get_Lines method


Represents an estimate of the number of lines in the document.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines()
```

## Remarks


Aspose.Words updates this property when you call [UpdateWordCount()](../../../aspose.words/document/updatewordcount/).

## Examples



Shows how to update all list labels in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words does not track document metrics like these in real time.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// To get accurate values for three of these properties, we will need to update them manually.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// For the line count, we will need to call a specific overload of the updating method.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
