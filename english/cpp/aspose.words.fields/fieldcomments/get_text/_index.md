---
title: Aspose::Words::Fields::FieldComments::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldComments::get_Text method. Gets or sets the text of the comments in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Gets or sets the text of the comments.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Examples



Shows how to use the COMMENTS field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set a value for the document's "Comments" built-in property.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Create a COMMENTS field to display the value of that built-in property.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// If we give the COMMENTS field's Text property value and update it, the field will
// overwrite the current value of the "Comments" built-in property with the value of its Text property,
// and then display the new value.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## See Also

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
