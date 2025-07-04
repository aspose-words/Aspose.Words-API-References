---
title: Aspose::Words::Fields::FieldChar::get_IsLocked method
linktitle: get_IsLocked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldChar::get_IsLocked method. Gets or sets whether the parent field is locked (should not recalculate its result) in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fields/fieldchar/get_islocked/
---
## FieldChar::get_IsLocked method


Gets or sets whether the parent field is locked (should not recalculate its result).

```cpp
bool Aspose::Words::Fields::FieldChar::get_IsLocked() const
```


## Examples



Shows how to work with a [FieldStart](../../fieldstart/) node. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Retrieve the facade object which represents the field in the document.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Update the field to show the current date.
field->Update();
```

## See Also

* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
