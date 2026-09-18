---
title: "Aspose::Words::Fields::Field::get_Result Methode"
linktitle: "get_Result"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field::get_Result Methode. Gibt den Text zurück oder setzt ihn, der zwischen dem Feldtrennzeichen und dem Feldende in C++ liegt."
type: docs
weight: 10000
url: /de/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Beispiele



Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Siehe auch

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
