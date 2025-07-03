---
title: Aspose::Words::Fields::Field::get_DisplayResult method
linktitle: get_DisplayResult
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::get_DisplayResult method. Gets the text that represents the displayed field result in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Gets the text that represents the displayed field result.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Examples



Shows how to get the real text that a field displays in the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// We can use the DisplayResult property to verify what exact text
// a field would display in its place in the document.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Fields do not maintain accurate result values in real-time.
// To make sure our fields display accurate results at any given time,
// such as right before a save operation, we need to update them manually.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
