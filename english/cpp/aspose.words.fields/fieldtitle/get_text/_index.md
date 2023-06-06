---
title: Aspose::Words::Fields::FieldTitle::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldTitle::get_Text method. Gets or sets the text of the title in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Gets or sets the text of the title.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Examples



Shows how to use the TITLE field. 
```cpp
auto doc = MakeObject<Document>();

// Set a value for the "Title" built-in document property.
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// We can use the TITLE field to display the value of this property in the document.
auto builder = MakeObject<DocumentBuilder>(doc);
auto field = System::ExplicitCast<FieldTitle>(builder->InsertField(FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Setting a value for the field's Text property,
// and then updating the field will also overwrite the corresponding built-in property with the new value.
builder->Writeln();
field = System::ExplicitCast<FieldTitle>(builder->InsertField(FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.TITLE.docx");
```

## See Also

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
