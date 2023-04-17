---
title: Aspose::Words::Fields::FieldChar::get_FieldType method
linktitle: get_FieldType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldChar::get_FieldType method. Returns the type of the field in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldchar/get_fieldtype/
---
## FieldChar::get_FieldType method


Returns the type of the field.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FieldChar::get_FieldType() const
```


## Examples



Shows how to work with a [FieldStart](../../fieldstart/) node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto field = System::DynamicCast<FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

SharedPtr<FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Retrieve the facade object which represents the field in the document.
field = System::DynamicCast<FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Update the field to show the current date.
field->Update();
```

## See Also

* Enum [FieldType](../../fieldtype/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
