---
title: Aspose::Words::Fields::FieldChar::GetField method
linktitle: GetField
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldChar::GetField method. Returns a field for the field char in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldchar/getfield/
---
## FieldChar::GetField method


Returns a field for the field char.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldChar::GetField()
```


### ReturnValue

A field for the field char.

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

* Class [Field](../../field/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
