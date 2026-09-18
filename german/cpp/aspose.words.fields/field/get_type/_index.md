---
title: "Aspose::Words::Fields::Field::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field::get_Type Methode. Gibt den Microsoft‑Word‑Feldtyp in C++ zurück."
type: docs
weight: 13000
url: /de/cpp/aspose.words.fields/field/get_type/
---
## Field::get_Type method


Liefert den Microsoft‑Word-Feldtyp.

```cpp
virtual Aspose::Words::Fields::FieldType Aspose::Words::Fields::Field::get_Type() const
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

* Enum [FieldType](../../fieldtype/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
