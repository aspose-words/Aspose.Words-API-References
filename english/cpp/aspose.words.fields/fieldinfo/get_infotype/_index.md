---
title: Aspose::Words::Fields::FieldInfo::get_InfoType method
linktitle: get_InfoType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldInfo::get_InfoType method. Gets or sets the type of the document property to insert in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Gets or sets the type of the document property to insert.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## Examples



Shows how to work with INFO fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set a value for the "Comments" built-in property and then insert an INFO field to display that property's value.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Setting a value for the field's NewValue property and updating
// the field will also overwrite the corresponding built-in property with the new value.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## See Also

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
