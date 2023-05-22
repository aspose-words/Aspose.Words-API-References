---
title: Aspose::Words::Fields::Field::get_Result method
linktitle: get_Result
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::get_Result method. Gets or sets text that is between the field separator and field end in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Gets or sets text that is between the field separator and field end.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Examples



Shows how to insert a field into a document using a field code. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
ASSERT_LE(System::Math::Abs((System::DateTime::Parse(field->get_Result()) - System::DateTime::get_Today()).get_Hours()), 24);
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
