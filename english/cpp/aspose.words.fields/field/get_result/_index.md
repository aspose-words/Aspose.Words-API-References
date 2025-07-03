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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
