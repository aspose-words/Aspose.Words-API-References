---
title: get_DisplayResult
second_title: Aspose.Words for C++ API Reference
description: Gets the text that represents the displayed field result.
type: docs
weight: 1
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::DynamicCast<FieldAuthor>(builder->InsertField(FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// We can use the DisplayResult property to verify what exact text
// a field would display in its place in the document.
ASSERT_EQ(String::Empty, fieldAuthor->get_DisplayResult());

// Fields do not maintain accurate result values in real-time.
// To make sure our fields display accurate results at any given time,
// such as right before a save operation, we need to update them manually.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(ArtifactsDir + u"Field.DisplayResult.docx");
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
