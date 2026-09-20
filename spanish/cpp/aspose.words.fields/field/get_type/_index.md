---
title: "Aspose::Words::Fields::Field::get_Type method"
linktitle: "get_Type"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::Field::get_Type method. Obtiene el tipo de campo de Microsoft Word en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.fields/field/get_type/
---
## Field::get_Type method


Obtiene el tipo de campo de Microsoft Word.

```cpp
virtual Aspose::Words::Fields::FieldType Aspose::Words::Fields::Field::get_Type() const
```


## Ejemplos



Muestra cómo insertar un campo en un documento usando un código de campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Ver también

* Enum [FieldType](../../fieldtype/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
