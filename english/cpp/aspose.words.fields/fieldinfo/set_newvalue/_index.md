---
title: Aspose::Words::Fields::FieldInfo::set_NewValue method
linktitle: set_NewValue
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldInfo::set_NewValue method. Sets an optional value that updates the property in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fields/fieldinfo/set_newvalue/
---
## FieldInfo::set_NewValue method


Sets an optional value that updates the property.

```cpp
void Aspose::Words::Fields::FieldInfo::set_NewValue(const System::String & value)
```

## Examples


Shows how to work with INFO fields.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set a value for the "Comments" built-in property and then insert an INFO field to display that property's value.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(field->GetFieldCode(), u" INFO  Comments");
ASSERT_EQ(field->get_Result(), u"My comment");

builder->Writeln();

// Setting a value for the field's NewValue property and updating
// the field will also overwrite the corresponding built-in property with the new value.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(field->GetFieldCode(), u" INFO  Comments \"New comment\"");
ASSERT_EQ(field->get_Result(), u"New comment");
ASSERT_EQ(doc->get_BuiltInDocumentProperties()->get_Comments(), u"New comment");

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```
## See Also

* [get_NewValue](../get_newvalue/)

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
