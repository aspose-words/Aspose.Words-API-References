---
title: "Aspose::Words::Fields::Field::get_Result method"
linktitle: "get_Result"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field::get_Result method. Hämtar eller anger text som ligger mellan fältseparatorn och fältets slut i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Exempel



Visar hur man infogar ett fält i ett dokument med en fältkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Denna överlagring av InsertField‑metoden uppdaterar automatiskt infogade fält.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
