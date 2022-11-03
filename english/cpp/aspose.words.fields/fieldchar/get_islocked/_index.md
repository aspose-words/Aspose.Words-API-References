---
title: get_IsLocked
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether the parent field is locked (should not recalculate its result).
type: docs
weight: 27
url: /cpp/aspose.words.fields/fieldchar/get_islocked/
---
## FieldChar.get_IsLocked method


Gets or sets whether the parent field is locked (should not recalculate its result).

```cpp
bool Aspose::Words::Fields::FieldChar::get_IsLocked() const
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
