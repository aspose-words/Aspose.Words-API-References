---
title: get_Text
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the text of the comments.
type: docs
weight: 1
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set a value for the document's "Comments" built-in property.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Create a COMMENTS field to display the value of that built-in property.
auto field = System::DynamicCast<FieldComments>(builder->InsertField(FieldType::FieldComments, true));
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

doc->Save(ArtifactsDir + u"Field.COMMENTS.docx");
```

## See Also

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
