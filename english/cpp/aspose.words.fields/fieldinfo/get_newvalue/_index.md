---
title: Aspose::Words::Fields::FieldInfo::get_NewValue method
linktitle: get_NewValue
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldInfo::get_NewValue method. Gets or sets an optional value that updates the property in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fieldinfo/get_newvalue/
---
## FieldInfo::get_NewValue method


Gets or sets an optional value that updates the property.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_NewValue()
```


## Examples



Shows how to work with INFO fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set a value for the "Comments" built-in property and then insert an INFO field to display that property's value.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::DynamicCast<FieldInfo>(builder->InsertField(FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Setting a value for the field's NewValue property and updating
// the field will also overwrite the corresponding built-in property with the new value.
field = System::DynamicCast<FieldInfo>(builder->InsertField(FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(ArtifactsDir + u"Field.INFO.docx");
```

## See Also

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
