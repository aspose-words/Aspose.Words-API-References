---
title: Aspose::Words::Fields::FieldChar::get_FieldType method
linktitle: get_FieldType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldChar::get_FieldType method. Returns the type of the field in C++.'
type: docs
weight: 5750
url: /cpp/aspose.words.fields/fieldchar/get_fieldtype/
---
## FieldChar::get_FieldType method


Returns the type of the field.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FieldChar::get_FieldType() const
```

## Examples


Shows how to work with a FieldStart node.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(fieldStart->get_FieldType(), FieldType::FieldDate);
ASPOSE_ASSERT_EQ(fieldStart->get_IsDirty(), false);
ASPOSE_ASSERT_EQ(fieldStart->get_IsLocked(), false);

// Retrieve the facade object which represents the field in the document.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(field->get_IsLocked(), false);
ASSERT_EQ(field->GetFieldCode(), (u" DATE  \\@ \"dddd, MMMM dd, yyyy\""));

// Update the field to show the current date.
field->Update();
```
## See Also

* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
