---
title: Aspose::Words::Fields::Field::get_IsLocked method
linktitle: get_IsLocked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::get_IsLocked method. Gets or sets whether the field is locked (should not recalculate its result) in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.fields/field/get_islocked/
---
## Field::get_IsLocked method


Gets or sets whether the field is locked (should not recalculate its result).

```cpp
bool Aspose::Words::Fields::Field::get_IsLocked()
```


## Examples



Shows how to work with a [FieldStart](../../fieldstart/) node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto field = System::ExplicitCast<FieldDate>(builder->InsertField(FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

SharedPtr<FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Retrieve the facade object which represents the field in the document.
field = System::ExplicitCast<FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Update the field to show the current date.
field->Update();
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
